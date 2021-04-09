<template>
	<div class="work">
		<Background parent="parent--work"></Background>
		<work-contents></work-contents>
	</div>
</template>

<script>
import Background from "@/components/Background";
import WorkContents from "@/components/Work/WorkContents";
export default {
	name: 'Work',
	components: {WorkContents, Background}
}
</script>
