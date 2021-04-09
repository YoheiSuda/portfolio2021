<template>
<div class="profile">
	<Background parent="parent--profile"></Background>
	<ProfileContents></ProfileContents>
</div>
</template>

<script>
import Background from "@/components/Background";
import ProfileContents from "@/components/Profile/ProfileContents";
export default {
name: "Profile",
	components: {ProfileContents, Background}
}
</script>

<style scoped>

</style>
