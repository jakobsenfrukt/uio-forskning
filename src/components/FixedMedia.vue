<template>
  <div class="figure item">
    <figure>
      <img :src="image" />
      <div class="caption-wrapper" v-for="(caption, index) in captions" :key="`caption-${index}`">
        <figcaption>
          {{ caption }}
        </figcaption>
      </div>
    </figure>
  </div>
</template>

<script>
export default {
  name: 'Figure',
  props: {
    image: String,
    captions: Array,
    alt: String
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

div {
  margin: 0 auto 4rem;
  width: 100%;
  position: relative;

  figure {
    margin: 0;
    padding: 0;
    position: relative;
  }

  img {
    position: sticky;
    top: 0;
    height: 100vh;
    width: 100%;
    object-fit: cover;
    z-index: 1000;
  }

  .caption-wrapper {
    height: 100vh;
    z-index: 1001;
  }

  figcaption {
    padding: 0.6rem 1rem;
    max-width: $width-s;
    margin: -1rem auto;
    position: relative;
    background: $color-black;
    color: $color-white;
  }
}
</style>
