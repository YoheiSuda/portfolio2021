<template>
	<div id="app">
		<router-view></router-view>
	</div>
</template>

<script>

export default {
	name: 'App',
	components: {
	}
}
</script>

<style lang="scss">
@import "assets/css/reset.css";

#app {
	position: relative;
	width: 100%;
	height: auto;
}
</style>
