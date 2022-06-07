<template>
  <!-- v-show="!isLoaded" -->
  <div class="spinner">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
  </div>
</template>

<script>
export default {
  name: "LoaderPage",
  data: () => {
    return {
      isLoaded: false,
    };
  },
  mounted() {
    document.onreadystatechange = () => {
      if (document.readyState == "complete") {
        this.isLoaded = true;
      }
    };
  },
};
</script>


<style lang="scss" scoped>
.spinner {
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  background-color: var(--clr-bg-0);
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  z-index: 1;

  @for $i from 1 to 5 {
    .box:nth-child(#{$i}) {
      animation: animatename 1s linear infinite;
      animation-delay: #{$i}s;
    }
  }
}

.box {
  height: 50px;
  aspect-ratio: 1/1;
  background-color: black;
}

@keyframes animatename {
  0% {
    transform: scale(1);
  }

  50% {
    transform: scale(1.5);
  }
}
</style>

