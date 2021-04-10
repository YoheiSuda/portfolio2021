<template>
	<div class="skill">
		<Background parent="parent--skill"></Background>
		<skill-contents></skill-contents>
	</div>
</template>

<script>
import Background from "@/components/Background";
import SkillContents from "@/components/Skill/SkillContents";

export default {
	name: "Skill",
	components: {SkillContents, Background}
}
</script>

<style scoped>

</style>
