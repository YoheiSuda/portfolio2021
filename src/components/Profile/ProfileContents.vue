<template>
	<div class="profileContents">
		<div class="profileContents__title">
			<h2>プロフィール</h2>
		</div>
		<div class="profileContents__pt01">
			<ul class="ul01">
				<li class="li01">
					<dl>
						<dt>名前：</dt>
						<dd>
							須田 耀平
						</dd>
					</dl>
				</li>
				<li class="li01">
					<dl>
						<dt>職業：</dt>
						<dd>
							フロントエンドエンジニア（今は<a href="https://www.dip-net.co.jp/" target="_blank">ここ</a>で働いてるよ）
						</dd>
					</dl>
				</li>
				<li class="li01">
					<dl>
						<dt>趣味：</dt>
						<dd>音楽制作/プログラミング/デザイン制作</dd>
					</dl>
				</li>
				<li class="li01">
					<dl>
						<dt>影響を受けた音楽：</dt>
						<dd>YMO/P-model/mad capsule markets/Number girl/eastern youth/sonic youth/asian kung-fu generation/Beat Crusaders/Elle garden/Dress codes/Tofubeats/長谷川白紙/崎山蒼志</dd>
					</dl>
				</li>
			</ul>
		</div>
	</div>
</template>

<script>
export default {
	name: "ProfileContents"
}
</script>

<style lang="scss" scoped>
.profileContents {
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
