<template>
  <section class="multi-column">
    <div v-for="(block, index) in blocks" :key="`block-${index}`" class="multi-column-block">
      <div class="image">
        <Figure
          :image="block.image"
          alt="Bildet viser no greier"
          size="full"
        />
      </div>
      <div class="text">
        <h3>
          <a v-if="block.link" :href="block.link">{{ block.heading }}</a>
          <template v-else>{{ block.heading }}</template>
        </h3>
        <p>{{ block.text }}</p>
      </div>
    </div>
  </section>
</template>

<script>
import Figure from '@/components/Figure.vue'

export default {
  name: 'MultiColumn',
  components: {
    Figure
  },
  props: {
    blocks: Array
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

.multi-column {
  width: $width-xl;
  max-width: 100%;
  margin: 1rem auto;
  display: flex;
  align-items: flex-start;
  flex-wrap: wrap;

  &-block {
    max-width: 33%;
    display: block;
    padding-right: 2rem;
  }

  h3 {
    font-size: 1.3rem;
    margin: 0.5rem auto;
  }

  p {
    font-size: $font-s;
  }

  /deep/ img {
    width: 100%;
    height: 8rem;
    object-fit: cover;
  }

  .figure {
    margin: 0;
  }

  @media (max-width: $media-s) {
    margin: 1rem auto 2rem;
    padding: 0;
    &-block {
      max-width: 100%;
      display: flex;
      padding-right: 0;
      margin-top: 1rem;

      .image {
        width: 30%;
      }
      .text {
        width: 70%;
        padding-left: 1rem;
      }
    }
  }
}

</style>
