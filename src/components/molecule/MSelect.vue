<template>
  <select name="type" id="type" @change="switchSelect(e)">
    <option value="" selected>All</option>
    <option v-for="(tag, idx) in select.tag" :key="idx" value="tag">
      {{ tag }}
    </option>
  </select>
</template>

<script>
import select from "../../global/Select";
export default {
  name: "MSelect",
  data() {
    return {
      select,
    };
  },
  methods: {
    switchSelect(e) {
      console.log(e.target.value);
    },
  },
};
</script>

<style>
</style>