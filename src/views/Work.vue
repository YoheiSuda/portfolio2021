<template>
	<div class="work">
		<Background parent="parent--work"></Background>
		<Header></Header>
	</div>
</template>

<script>
import Header from "@/components/Header";
import Background from "@/components/Background";
export default {
	name: 'Work',
	components: {Background, Header}
}
</script>
