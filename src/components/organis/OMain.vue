<template>
  <main>
    <div class="container">
      <MCard v-for="(track, idx) in tracks" :key="idx" :track="track" />
    </div>
  </main>
</template>

<script>
import axios from "axios";
import MCard from "../molecule/MCard.vue";

export default {
  components: { MCard },
  name: "OMain",
  data() {
    return {
      tracks: [],
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((response) => {
        console.log(response.data.response);
        this.tracks = response.data.response;
      })
      .catch((e) => {
        console.log(e);
      });
  },
};
</script>

<style lang="scss" scoped>
main {
  padding: var(--padding-xl);
  background-color: var(--clr-bg-1);
  min-height: calc(100vh - var(--hgt-header));
  display: flex;
  justify-content: center;
}
.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
  gap: 1.2rem;
}
</style>