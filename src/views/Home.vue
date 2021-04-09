<template>
	<div class="home">
		<background parent="parent--home"></background>
	</div>
</template>

<script>
import Background from "@/components/Background";

export default {
	name: 'Home',
	components: {
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
