<template>
	<div id="app">
		<Header></Header>
		<router-view></router-view>
	</div>
</template>

<script>

import Header from "@/components/Header";
export default {
	name: 'App',
	components: {
		Header
	}
}
</script>

<style lang="scss">
@import "assets/css/reset.css";

#app {
	position: relative;
	width: 100%;
	height: auto;
	line-height: 1.5;
	a {
		color: #000;
		transition: all 0.1s;
		&:hover {
			color: #fff;
			background: rgb(63,94,251);
			background: linear-gradient(90deg, rgba(63,94,251,1) 0%, rgba(252,70,107,1) 100%);
		}
	}
}
</style>
