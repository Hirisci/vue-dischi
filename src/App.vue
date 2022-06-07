<template>
  <div id="app">
    <OHeader />
    <OMain />
  </div>
</template>

<script>
import OHeader from "./components/organis/OHeader.vue";
import OMain from "./components/organis/OMain.vue";
export default {
  name: "App",
  components: { OHeader, OMain },
};
</script>

<style lang="scss">
@import "./assets/style/style.scss";
</style>
