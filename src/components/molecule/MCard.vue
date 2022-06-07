<template>
  <div class="card">
    <AImg class="card_img" :src="track.poster" :alt="track.title" />
    <ATextTitle class="card_title" tag="h5" :text="track.title" />
    <AText class="card_text" tag="p" :text="track.author" />
  </div>
</template>

<script>
import AImg from "../atom/AImg.vue";
import AText from "../atom/AText.vue";
import ATextTitle from "../atom/ATextTitle.vue";
export default {
  components: { AImg, ATextTitle, AText },
  name: "MCard",
  props: {
    track: Object,
  },
};
</script>

<style lang="scss" scoped>
.card {
  @include flex();
  padding: var(--padding-md);
  background-color: var(--clr-bg-0);
  justify-content: space-between;
  color: var(--clr-text-1);
  gap: 1rem;
  text-align: center;
  &_img {
    width: 100%;
    aspect-ratio: 1/1;
  }
  &_title {
    text-transform: uppercase;
  }
  &_text {
    opacity: 0.5;
  }
}
</style>