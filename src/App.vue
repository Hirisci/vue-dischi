<template>
  <div id="app">
    <OHeader />
  </div>
</template>

<script>
import OHeader from "./components/organis/OHeader.vue";
export default {
  name: "App",
  components: { OHeader },
};
</script>

<style lang="scss">
@import "./assets/style/style.scss";
</style>
