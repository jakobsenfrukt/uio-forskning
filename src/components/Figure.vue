<template>
  <figure class="full">
    <img :src="image" />
    <figcaption v-if="caption">
      {{ caption }}
    </figcaption>
  </figure>
</template>

<script>
export default {
  name: 'Figure',
  props: {
    image: String,
    caption: String,
    alt: String
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

figure {
  margin: 0;
  padding: 0;

  &.full {
    width: 100%;
    margin-top: 4rem;

    &:first-child {
      margin-top: 0;
    }

    img {
      width: 100%;
    }
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
