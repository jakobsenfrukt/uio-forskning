<template>
  <div class="figure item" :class="size">
    <figure>
      <img :src="image" />
      <figcaption v-if="caption">
        {{ caption }}
        <span class="photoby">Foto: Svein Stølen</span>
      </figcaption>
    </figure>
  </div>
</template>

<script>
export default {
  name: 'Figure',
  props: {
    image: String,
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
  }

  &.full {
    width: 100%;
  }

  &.column {
    width: $width-s;

    figure {
      margin: 0 -2rem;
      @media (max-width: $media-s) {
        margin: 0 1rem;
      }
    }
  }

  &.split {
    width: $width-l;
    margin-top: 3rem;

    figure {
      display: flex;
      align-items: center;
    }

    img {
      width: 50%;
      display: block;
      align-self: center;
      padding-right: 1rem;
    }

    figcaption {
      margin: 0;
      width: 50%;
      background: none;
      color: $color-black;
      line-height: 1.6;
      font-style: italic;
      font-family: $serif;
      font-size: 1rem;
    }

    .photoby {
      text-align: left;
      margin-top: 1rem;
    }

    &.reverse {
      text-align: right;
      figcaption {
        order: 1;
      }
      img {
        order: 2;
        padding-right: 0;
        padding-left: 1rem;
      }
      .photoby {
        text-align: right;
      }
    }

    @media (max-width: $media-s) {
      margin: 1rem auto 2rem;
      padding: 0 1rem;
      figure {
        display: block;
      }

      img, figcaption,
      &.reverse figcaption, &.reverse img {
        width: 100%;
        padding-left: 0;
        padding-right: 0;
      }
    }
  }

  &.quote {
    figcaption {
      font-style: italic;
      font-family: $serif;
    }
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

  .photoby {
    font-size: $font-xs;
    display: block;
    font-style: italic;
    text-align: right;
    font-family: sans-serif;
  }

  @media (max-width: $media-s) {
    margin-bottom: 2rem;
  }
}
</style>
