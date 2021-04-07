<template>
	<div class="home">
		<background parent="parent--home"></background>
		<Header></Header>
	</div>
</template>

<script>
import Background from "@/components/Background";
import Header from "@/components/Header";

export default {
	name: 'Home',
	components: {
		Header,
		Background
	}
}
</script>

<style lang="scss" scoped>
.home {
	position: relative;
	width: 100%;
	height: auto;
}
</style>
