<template>
	<div class="workContents">
		<div class="workContents__bg">
		</div>
		<div class="workContents__wrap">
			<div class="workContents__title">
				<h2>（個人的に）今までやってきたコト</h2>
			</div>
			<div class="workContents__pt01">
				<ul class="ul01">
					<li class="li01">
						<a href="https://seiza-uranai.jp/" target="_blank">
							GASと連携し、全自動投稿機能を付けた星座占いサイト(ライトスタッフ合同会社に売却済)	
						</a>
					</li>
					<li class="li01">
						<a href="https://tatolol-tools.tech/convert-img/" target="_blank">
							画像変換ツール（クライアントサイド）
						</a>
					</li>
					<li class="li01">
						<a href="https://github.com/YoheiSuda/mailgo" target="_blank">
							OSSコミット：mailgoのi18n対応（日本語化）を担当
						</a>
					</li>
					<li class="li01">
						<a href="http://tatolol.me/kmnz_css_animation/" target="_blank">
							KMNZのCSSアニメーション
						</a>
					</li>
					<li class="li01">
						<a href="https://tatolol.me/christmas_css/dist/" target="_blank">
							クリスマスっぽいcssアニメーション作成
						</a>
					</li>
					<li class="li01">
						<a href="https://tatolol.me/my-transform-feedback-sample/" target="_blank">
							webgl2のtransform-feedbackを使ってみた
						</a>
					</li>
					<li class="li01">
						<a href="https://pixabaylgtm.herokuapp.com/" target="_blank">
							pixabay apiを利用して適当にlgtmしたいがための自己満サービス
						</a>
					</li>
					<li class="li01">
						<a href="https://tatolol.me/omesis_cssmv/" target="_blank">
							おめがシスターズのcssアニメーション
						</a>
					</li>
					<li class="li01">
						<a href="https://www.chuo.ac.jp/np/051.pdf" target="_blank">
							Vue.js + webglでGLSLsandboxライクなGLSLEditor開発（現状は非公開のため、専門学校の卒制であげた記事のみ貼っておきます）
						</a>
					</li>
					<li class="li01">
						<a href="https://qetic.jp/music/bornnow-pickup/294500/" target="_blank">
							BornNow 2018にvjとして参加
						</a>
					</li>
					<li class="li01">
						<a href="https://qiita.com/tato_lol" target="_blank">
							qiitaの記事
						</a>
					</li>
					<li class="li01">
						<a href="https://developer.dip-net.co.jp/entry/%E3%82%AC%E3%82%BF%E3%81%A4%E3%81%8D%E3%81%AE%E3%81%AA%E3%81%84%E9%AB%98%E3%81%95%E5%8F%AF%E5%A4%89%E3%81%AE%E3%82%AB%E3%83%AB%E3%83%BC%E3%82%BB%E3%83%AB%E3%82%B9%E3%83%A9%E3%82%A4%E3%83%80%E3%83%BC" target="_blank">
							ディップのエンジニアブログ記事（カルーセルスライド実装周り）
						</a>
					</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "WorkContents"
}
</script>

<style lang="scss" scoped>
@import "../../assets/css/colorPalette.scss";

.workContents {
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
		background: $yellow01;
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
		@media screen and (max-width: 768px) {
			padding: 32px 0 0;
		}
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
