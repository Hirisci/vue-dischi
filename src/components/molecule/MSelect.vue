<template>
  <div class="box">
    <ATextTitle tag="h6" text="Scegli il tuo genere" />
    <select name="type" id="type" v-model="select.value">
      <option value="" selected>All</option>
      <option v-for="(tag, idx) in select.tag" :key="idx" :value="tag">
        {{ tag }}
      </option>
    </select>
  </div>
</template>

<script>
import select from "../../global/Select";
import ATextTitle from "../atom/ATextTitle.vue";
export default {
  components: { ATextTitle },
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

<style lang="scss" scoped>
.box {
  color: var(--clr-text-1);
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  font-weight: 400;
}
</style>