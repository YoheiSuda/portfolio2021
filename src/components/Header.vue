<template>
	<div class="header">
		<div class="header__flex">
			<div class="header__title">
				<router-link to="/">
					<span class="span01"></span><span class="span02"></span><span class="span03"></span><span class="span04"></span>
				</router-link>
			</div>
			<div class="header__time">
				<Clock></Clock>
			</div>
		</div>
	</div>
</template>

<script>
import Clock from "@/components/Header/Clock";
export default {
	name: "Header",
	components: {Clock}
}
</script>

<style lang="scss" scoped>
@import "../assets/css/colorPalette.scss";
// keyframes
@keyframes changeLetter1 {
	0% {
		content: "須";
	}
	70% {
		content: "須";
	}
	75% {
		content: "好";
	}
	80% {
		content: "数";
	}
	85% {
		content: "巣";
	}
	90% {
		content: "素";
	}
	95% {
		content: "捨";
	}
	100% {
		content: "す";
	}
}
@keyframes changeLetter2 {
	0% {
		content: "田";
	}
	70% {
		content: "田";
	}
	75% {
		content: "多";
	}
	80% {
		content: "垂";
	}
	85% {
		content: "断";
	}
	90% {
		content: "丹";
	}
	95% {
		content: "駄";
	}
	100% {
		content: "た";
	}
}
@keyframes changeLetter3 {
	0% {
		content: "耀";
	}
	70% {
		content: "耀";
	}
	75% {
		content: "陽";
	}
	80% {
		content: "幼";
	}
	85% {
		content: "酔";
	}
	90% {
		content: "葉";
	}
	95% {
		content: "蓉";
	}
	100% {
		content: "よ";
	}
}
@keyframes changeLetter4 {
	0% {
		content: "平";
	}
	70% {
		content: "平";
	}
	75% {
		content: "閉";
	}
	80% {
		content: "睥";
	}
	85% {
		content: "丙";
	}
	90% {
		content: "幣";
	}
	95% {
		content: "塀";
	}
	100% {
		content: "へ";
	}
}
.header {
	position: fixed;
	width: 100%;
	padding: 32px;
	background: #eeeeee;
	z-index: 999;
	&__flex {
		position: relative;
		display: flex;
		justify-content: space-between;
		align-items: center;
		width: 100%;
		height: auto;
	}
	&__title {
		position: relative;
		width: auto;
		height: auto;
		a {
			display: block;
		}
		span {
			font-size: 32px;
			&.span01 {
				&::after {
					content: "須";
					animation: changeLetter1 1s linear 0.8s infinite;
				}
			}
			&.span02 {
				&::after {
					content: "田";
					animation: changeLetter2 1s linear 1s infinite;
				}
			}
			&.span03 {
				&::after {
					content: "耀";
					animation: changeLetter3 1s linear 1.2s infinite;
				}
			}
			&.span04 {
				&::after {
					content: "平";
					animation: changeLetter4 1s linear 1.4s infinite;
				}
			}
		}
	}
	&__time {
	}
}
</style>
