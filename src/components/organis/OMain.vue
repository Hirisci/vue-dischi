<template>
  <main>
    <div class="container">
      <MCard v-for="(track, idx) in filterTracks" :key="idx" :track="track" />
    </div>
  </main>
</template>

<script>
import axios from "axios";
import MCard from "../molecule/MCard.vue";
import select from "../../global/Select";

export default {
  components: { MCard },
  name: "OMain",
  data() {
    return {
      tracks: [],
      select,
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((response) => {
        this.tracks = response.data.response;
      })
      .catch((e) => {
        console.log(e);
      });
  },
  computed: {
    filterTracks() {
      if (this.select.value === "") {
        return this.tracks;
      }

      return this.tracks.filter((elm) => elm.genre === this.select.value);
    },
    tagTracks() {
      let arr = [];
      this.tracks.forEach((elm) => {
        if (!arr.includes(elm.genre)) {
          arr.push(elm.genre);
        }
      });
      select.tag = arr;
      return arr;
    },
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