<template>
  <div class="hero">
  <!--<div class="hero" :style="{ 'background-image': 'url(' + image + ')' }">-->
    <img :src="image" />
    <div class="overlay">
      <transition name="fadeup" appear>
      <div class="text">
        <h1>{{ heading }}</h1>
        <span class="subhead">RITMO - Centre for Interdisciplinary Studies in Rhythm, Time and Motion</span>
      </div>
      </transition>
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
  margin: 0 auto 2rem;
  position: relative;
  min-height: 60vh;

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
    max-width: 100%;
    margin: 0 auto;
    color: white;
    text-shadow: 0 0 0.5rem rgba(0, 0, 0, 0.8);
  }
  h1 {
    margin-bottom: 0;
  }
  .subhead {
    font-size: $font-s;
    line-height: 1.2;
    display: block;
    margin: 0.5rem 0 1.6rem;
  }

  @media (max-width: $media-s) {
    .text {
      padding: 0 1rem;
    }
  }
}
</style>
