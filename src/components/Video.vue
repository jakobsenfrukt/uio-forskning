<template>
  <div class="video" :class="size">
    <video v-if="controls" controls>
      <source :src="video" type="video/mp4">
    </video>
    <video v-else muted autoplay>
      <source :src="video" type="video/mp4">
    </video>
  </div>
</template>

<script>
export default {
  name: 'Video',
  props: {
    video: String,
    size: String,
    controls: Boolean
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

div {
  margin: 0 auto 4rem;
  max-width: 100%;

  &.full {
    width: 100%;
  }

  &.column {
    width: $width-s;
  }

  video {
    width: 100%;
  }

  @media (max-width: $media-s) {
    margin-bottom: 2rem;
  }
}
</style>
