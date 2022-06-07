<template>
  <div id="app">
    <LoaderPage />
    <OHeader />
    <OMain />
  </div>
</template>

<script>
import LoaderPage from "./components/loader/LoaderPage.vue";
import OHeader from "./components/organis/OHeader.vue";
import OMain from "./components/organis/OMain.vue";
export default {
  name: "App",
  components: { OHeader, OMain, LoaderPage },
};
</script>

<style lang="scss">
@import "./assets/style/style.scss";
#app {
  position: relative;
}
</style>
