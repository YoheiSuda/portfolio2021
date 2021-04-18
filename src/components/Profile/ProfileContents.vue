<template>
	<div class="profileContents">
		<div class="profileContents__bg">
		</div>
		<div class="profileContents__wrap">
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
						<dl class="dl01">
							<dt>影響を受けた音楽：</dt>
							<dd>YMO/P-model/mad capsule markets/Number girl/eastern youth/sonic youth/asian kung-fu generation/Beat Crusaders/Elle garden/Dress codes/Tofubeats/長谷川白紙/崎山蒼志</dd>
						</dl>
					</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "ProfileContents"
}
</script>

<style lang="scss" scoped>
@import "../../assets/css/colorPalette.scss";

.profileContents {
	position: relative;
	top: 112px;
	width: 900px;
	margin: auto;
	@media screen and (max-width: 910px) {
		width: 740px;
	}
	@media screen and (max-width: 768px) {
		width: 100%;
		padding-bottom: 10px;
	}
	&__bg {
		z-index: 0;
		position: absolute;
		background: $green01;
		width: 100%;
		height: 100%;
		top: 10px;
		left: 10px;
		@media screen and (max-width: 768px) {
			width: calc(100% - 10px);
			height: calc(100% - 10px);
			top: 10px;
			left: 10px;
		}
	}
	&__wrap {
		position: relative;
		background: #fff;
		padding: 32px;
		border: 1px solid #000;
		z-index: 10;
		@media screen and (max-width: 768px) {
			width: calc(100% - 10px);
		}
	}
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
		dl {
			display: flex;
			justify-content: flex-start;
			dt {
				width: 100px;
			}
			dd {
				width: calc(100% - 100px);
			}
		}
		.dl01 {
			display: block;
			dt {
				width: 100%;
			}
			dd {
				width: 100%;
			}
		}
		@media screen and (max-width: 768px) {
			padding: 32px 0 0;
			dl {
				display: block;
			}
		}
	}
}
</style>
