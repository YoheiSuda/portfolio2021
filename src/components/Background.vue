<template>
	<div class="bg" v-bind:class=this.parent>
		<div class="bg__child01">
			<ul class="ul01">
				<li class="li01--gray"></li>
				<li class="li01--yellow">
					<router-link to="/work">Works</router-link>
				</li>
				<li class="li01--skyblue"></li>
				<li class="li01--green">
					<router-link to="/profile">Profile</router-link>
				</li>
				<li class="li01--pink"></li>
				<li class="li01--red">
					<router-link to="/skill">Skills</router-link>
				</li>
				<li class="li01--blue"></li>
			</ul>
		</div>
		<div class="bg__child02">
			<ul class="ul01">
				<li class="li01--blue"></li>
				<li class="li01--black"></li>
				<li class="li01--pink"></li>
				<li class="li01--black"></li>
				<li class="li01--skyblue"></li>
				<li class="li01--black"></li>
				<li class="li01--gray"></li>
			</ul>
		</div>
		<div class="bg__child03">
			<ul class="ul01">
				<li class="li01--blue2"></li>
				<li class="li01--white"></li>
				<li class="li01--purple"></li>
				<li class="li01--black"></li>
			</ul>
			<ul class="ul02">
				<li class="li02--blacks">
					<ul class="ul02a">
						<li class="li01--black2"></li>
						<li class="li01--black"></li>
						<li class="li01--black3"></li>
					</ul>
				</li>
				<li class="li01--black"></li>
			</ul>
		</div>
	</div>
</template>

<script>
export default {
	name: "Background",
	props : {
		parent : {
			type: String,
			default: 'parent--home'
		}
	},
	data() {
		return {

		}
	},
}
</script>

<style lang="scss" scoped>
@import "../assets/css/colorPalette.scss";
@keyframes fadeOut {
	0% {
		opacity: 1;
	}
	100% {
		opacity: 0;
	}
}

@keyframes fadeIn {
	0% {
		opacity: 0;
	}
	100% {
		opacity: 1;
	}
}

.bg {
	position: fixed;
	margin-top: 112px;
	width: 100%;
	height: calc(100vh - 112px);
	transition: all 0.3s;
	.li01--gray {
		background: $gray01;
	}
	.li01--yellow {
		background: $yellow01;
	}
	.li01--skyblue {
		background: $skyblue01;
	}
	.li01--green {
		background: $green01;
	}
	.li01--pink {
		background: $pink01;
	}
	.li01--red {
		background: $red01;
	}
	.li01--blue {
		background: $blue01;
	}
	.li01--blue2 {
		background: $blue02;
	}
	.li01--white {
		background: #fff;
	}
	.li01--purple {
		background: $purple01;
	}
	.li01--black {
		background: $black01;
	}
	.li01--black2 {
		background: $black02;
	}
	.li01--black3 {
		background: $black03;
	}
	&.parent--home {
		li {
			animation: fadeIn 1s linear 0s forwards;
		}
	}
	&.parent--work {
		opacity: 0.2;
		li {
			animation: fadeOut 1s linear 0s forwards;
			pointer-events: none;
		}
		.bg__child01 {
			.ul01 {
				.li01--yellow {
					animation: none;
				}
			}
		}
	}
	&.parent--profile {
		opacity: 0.2;
		li {
			animation: fadeOut 1s linear 0s forwards;
			pointer-events: none;
		}
		.bg__child01 {
			.ul01 {
				.li01--green {
					animation: none;
				}
			}
		}
	}
	&.parent--skill {
		opacity: 0.2;
		li {
			animation: fadeOut 1s linear 0s forwards;
			pointer-events: none;
		}
		.bg__child01 {
			.ul01 {
				.li01--red {
					animation: none;
				}
			}
		}
	}
	&__child01 {
		position: relative;
		width: 100%;
		height: 60%;
		.ul01 {
			position: relative;
			display: flex;
			justify-content: flex-start;
			width: 100%;
			height: 100%;
			> [class^="li01"] {
				width: calc(100% / 7);
				height: 100%;
				a {
					display: flex;
					justify-content: center;
					align-items: center;
					font-size: 32px;
					height: 100%;
				}
			}
		}
	}

	&__child02 {
		position: relative;
		width: 100%;
		height: 10%;
		.ul01 {
			position: relative;
			display: flex;
			justify-content: flex-start;
			width: 100%;
			height: 100%;
			> [class^="li01"] {
				width: calc(100% / 7);
				height: 100%;
			}
		}
	}

	&__child03 {
		position: relative;
		width: 100%;
		height: 30%;
		display: flex;
		justify-content: flex-start;
		.ul01 {
			position: relative;
			width: calc(100% - (100% / 7 * 2));
			height: 100%;
			display: flex;
			justify-content: flex-start;
			> [class^="li01"] {
				width: 25%;
				height: 100%;
			}
		}
		.ul02 {
			position: relative;
			width: calc(100% / 7 * 2);
			height: 100%;
			display: flex;
			justify-content: flex-start;
			> li {
				width: 50%;
				height: 100%;
			}
			.li02--blacks {
				position: relative;
				> .ul02a {
					position: relative;
					width: 100%;
					height: 100%;
					display: flex;
					justify-content: flex-start;
					> li {
						width: calc(100% / 3);
						height: 100%;
					}
				}
			}
		}
	}
}
</style>
