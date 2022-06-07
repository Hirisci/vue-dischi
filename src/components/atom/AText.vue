<template>
  <component :is="tag">{{ text }}</component>
</template>

<script>
export default {
  name: "AText",
  props: {
    tag: String,
    text: String,
  },
};
</script>


<style lang="scss" scoped>
</style>