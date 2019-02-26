<template>
  <div class="hero">
  <!--<div class="hero" :style="{ 'background-image': 'url(' + image + ')' }">-->
    <img :src="image" />
    <div class="overlay">
      <div class="text">
        <h1>{{ heading }}</h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero',
  props: {
    image: String,
    heading: String
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

.hero {
  margin: 0 auto 3rem;
  position: relative;

  /*height: 70vh;
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;*/

  img {
    width: 100%;
  }

  .overlay {
    position: absolute;
    top: 0; right: 0; bottom: 0; left: 0;
    background: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0), rgba(0, 0, 0, 1));

    display: flex;
    align-items: flex-end;
  }
  .text {
    width: $width-m;
    margin: 0 auto;
    color: white;
    text-shadow: 0 0 0.5rem rgba(0, 0, 0, 0.8);
  }
}
</style>
