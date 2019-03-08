<template>
  <div class="video item" :class="size">
    <figure>
      <iframe width="560" height="315" :src="video" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      <figcaption v-if="caption">
        {{ caption }}
      </figcaption>
    </figure>
  </div>
</template>

<script>
export default {
  name: 'Video',
  props: {
    video: String,
    caption: String,
    alt: String,
    size: String
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

div {
  margin: 0 auto 4rem;
  max-width: 100%;

  figure {
    margin: 0;
    padding: 0;
    position: relative;
    padding-bottom: 56.25%; /* 16:9 */
    padding-top: 25px;
    height: 0;
  }

  &.full {
    width: 100%;
  }

  &.column {
    width: $width-s;

    figure {
      margin: 0 -2rem;

      @media (max-width: $media-s) {
        margin: 0;
      }
    }
  }

  iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  figcaption {
    padding: 0.6rem 1rem;
    max-width: $width-s;
    margin: -1rem auto;
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    z-index: 10;
    background: $color-black;
    color: $color-white;

    font-size: $font-s;
  }

  @media (max-width: $media-s) {
    margin-bottom: 2rem;
  }
}
</style>
