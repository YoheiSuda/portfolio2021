<template>
  <div id="app">
    <background></background>
  </div>
</template>

<script>
import Background from "@/components/Background";

export default {
  name: 'App',
  components: {
    Background,
  }
}
</script>

<style lang="scss" scoped>
@import "assets/css/reset.css";

#app {
  position: relative;
  width: 100%;
  height: auto;
}
</style>
