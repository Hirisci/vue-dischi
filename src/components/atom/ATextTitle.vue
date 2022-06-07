<template>
  <component :is="tag">{{ text }}</component>
</template>

<script>
export default {
  name: "ATextTitle",
  props: {
    tag: String,
    text: String,
  },
};
</script>


<style lang="scss" scoped>
</style>