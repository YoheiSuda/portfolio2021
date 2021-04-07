<template>
	<div class="clock">
		<p>{{formattedDate}}</p>
	</div>
</template>

<script>
export default {
	name: "clock",
	data() {
		return {
			formattedDate: "9999/99/99 99:99:99"
		}
	},
	created() {
		let self = this;
		setInterval(function () {
			self.formattedDate = self.dateToFormatString(new Date(), '%YMD% %HH%:%mm%:%ss%');
		}, 1000);
	},
	methods: {
		dateToFormatString: function (date, fmt, locale, pad) {
			// %fmt% を日付時刻表記に。
			// 引数
			//  date:  Dateオブジェクト
			//  fmt:   フォーマット文字列、%YYYY%年%MM%月%DD%日、など。
			//  locale:地域指定。デフォルト（入力なし）の場合はja-JP（日本）。現在他に対応しているのはen-US（英語）のみ。
			//  pad:   パディング（桁数を埋める）文字列。デフォルト（入力なし）の場合は0。
			// 例：2016年03月02日15時24分09秒
			// %YYYY%:4桁年（2016）
			// %MM%:2桁月（03）
			// %DD%:2桁日（02）
			// %HH%:2桁で表した24時間表記の時（15）
			// %mm%:2桁分（24）
			// %ss%:2桁秒（09）
			var padding = function (n, d, p) {
				p = p || '0';
				return (p.repeat(d) + n).slice(-d);
			};
			var format = {
				'YMD': function() { return format.YYYY() + '/' + format.MM() + '/' + format.DD(); },
				'YYYY': function () {
					return padding(date.getFullYear(), 4, pad);
				},
				'MM': function () {
					return padding(date.getMonth() + 1, 2, pad);
				},
				'DD': function () {
					return padding(date.getDate(), 2, pad);
				},

				'HH': function () {
					return padding(date.getHours(), 2, pad);
				},
				'mm': function () {
					return padding(date.getMinutes(), 2, pad);
				},
				'ss': function () {
					return padding(date.getSeconds(), 2, pad);
				},
			};
			var fmtstr = ['']; // %%（%として出力される）用に空文字をセット。
			Object.keys(format).forEach(function (key) {
				fmtstr.push(key); // ['', 'YYYY', 'YY', 'MMMM',... 'W', 'w']のような配列が生成される。
			})
			var re = new RegExp('%(' + fmtstr.join('|') + ')%', 'g');
			// /%(|YYYY|YY|MMMM|...W|w)%/g のような正規表現が生成される。
			var replaceFn = function (match, fmt) {
				// match には%YYYY%などのマッチした文字列が、fmtにはYYYYなどの%を除くフォーマット文字列が入る。
				if (fmt === '') {
					return '%';
				}
				var func = format[fmt];
				// fmtがYYYYなら、format['YYYY']がfuncに代入される。つまり、
				// function() { return padding(date.getFullYear(), 4, pad); }という関数が代入される。
				if (func === undefined) {
					//存在しないフォーマット
					return match;
				}
				return func(locale);
			};
			return fmt.replace(re, replaceFn);
		}
	}
}

</script>

<style scoped>

</style>
