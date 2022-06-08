<template>
  <header>
    <ALogo />
    <MSelect />
  </header>
</template>

<script>
import ALogo from "../atom/ALogo.vue";
import MSelect from "../molecule/MSelect.vue";
export default {
  components: { ALogo, MSelect },
  name: "OHeader",
};
</script>

<style lang="scss" scoped>
header {
  display: flex;
  justify-content: space-between;
  background-color: var(--clr-bg-0);
  height: var(--hgt-header);
  padding: var(--padding-md);
}
</style>