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
  max-width: $width-l;
  margin: 4rem auto 6rem;
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
}
</style>
