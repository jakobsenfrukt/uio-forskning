<template>
  <div class="figure item" :class="size">
    <figure>
      <img :src="image" />
      <figcaption v-if="caption">
        {{ caption }}
      </figcaption>
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
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

div {
  margin: 0 auto 4rem;
  width: 100%;

  figure {
    margin: 0;
    padding: 0;
  }

  img {
    width: 100%;
  }

  figcaption {
    padding: 0.6rem 1rem;
    max-width: $width-s;
    margin: -1rem auto;
    position: relative;
    z-index: 10;
    background: $color-black;
    color: $color-white;

    font-size: $font-s;
  }
}
</style>
