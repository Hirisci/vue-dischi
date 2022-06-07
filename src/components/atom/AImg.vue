<template>
  <img :src="src" :alt="alt" />
</template>

<script>
export default {
  name: "AImg",
  props: {
    src: String,
    alt: String,
  },
};
</script>

<style lang="scss" scoped>
</style>