<template>
  <header>
    <ALogo />
  </header>
</template>

<script>
import ALogo from "../atom/ALogo.vue";
export default {
  components: { ALogo },
  name: "OHeader",
};
</script>

<style lang="scss" scoped>
header {
  background-color: var(--clr-bg-0);
  height: var(--hgt-header);
  padding: var(--padding-md);
}
</style>