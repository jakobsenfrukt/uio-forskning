<template>
  <blockquote class="quote item">
    {{ text }}
  </blockquote>
</template>

<script>
export default {
  name: 'Quote',
  props: {
    text: String
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

blockquote {
  width: $width-l;
  max-width: 100%;
  margin: 4rem auto 4.6rem;
  padding: 0 1rem;
  font-family: $serif;
  font-style: italic;
  font-size: 2rem;
  line-height: 1.4;
  text-align: center;

  &:before {
    content: "«";
  }
  &:after {
    content: "»";
  }

  @media (max-width: $media-s) {
    font-size: 1.3rem;
    margin: 1rem auto 2rem;
  }
}
</style>
