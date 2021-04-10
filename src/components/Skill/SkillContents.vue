<template>
	<div class="skillContents">
		<div class="skillContents__title">
			<h2>スキル</h2>
		</div>
		<div class="skillContents__pt01">
			<ul class="ul01">
				<li class="li01">
					<dl>
						<dt>HTML：</dt>
						<dd>
							HTML5でセマンティックなマークアップができる。<br>
							HTML4でメルマガ作成ができる。
						</dd>
					</dl>
				</li>
				<li class="li01">
					<dl>
						<dt>CSS：</dt>
						<dd>
							BEMを用いたcss設計ができる。<br>
							scssを使える。<br>
							cssアニメーションを使える。
						</dd>
					</dl>
				</li>
				<li class="li01">
					<dl>
						<dt>JavaScript：</dt>
						<dd>
							ES6基準のコードが書ける。<br>
							Vue.jsが使える。<br>
							競技プログラミングをJavaScriptで解ける。
						</dd>
					</dl>
				</li>
				<li class="li01">
					<dl>
						<dt>デザイン：</dt>
						<dd>
							XD/Illustrator/Photoshopをそこそこ使える。<br>
							figmaも使える。<br>
							UXを考慮したやり取りを企画側と行うことができる。
						</dd>
					</dl>
				</li>
				<li class="li01">
					<dl>
						<dt>保有資格：</dt>
						<dd>
							基本情報技術者<br>
							応用情報技術者<br>
							Oracle認定Java SE8 silver
						</dd>
					</dl>
				</li>
				<li class="li01">
					<dl>
						<dt>その他：</dt>
						<dd>
							学生時代はJavaやC言語を勉強していました。<br>
						</dd>
					</dl>
				</li>
			</ul>
		</div>
	</div>
</template>

<script>
export default {
name: "SkillContents"
}
</script>

<style lang="scss" scoped>
.skillContents {
	position: relative;
	top: 112px;
	width: 900px;
	margin: auto;
	padding: 56px 0;
	&__title {
		font-size: 32px;
	}
	&__pt01 {
		position: relative;
		width: 100%;
		margin: auto;
		padding: 56px 32px 0;
		.ul01 {
			.li01 {
				font-size: 24px;
			}
			.li01 + .li01 {
				margin-top: 16px;
			}
		}
	}
}
</style>
