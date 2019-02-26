<template>
  <section class="gallery">
    <div class="inner">
      <Figure
        image="https://dailystoic.com/wp-content/uploads/2018/01/diogenes.jpg"
        caption="Dette er en bildetekst! :)"
        alt="Bildet viser no greier"
        size="full"
      />
      <Figure
        image="http://piasa.info/wp-content/uploads/greek-philosophers-painting-ancient-greek-philosopher-tumblr-greek-philosophers-painting.jpg"
        caption="Dette er en bildetekst! :)"
        alt="Bildet viser no greier"
        size="full"
      />
      <Figure
        image="http://st2.ancientfacts.net/wp-content/uploads/2018/02/Philosophers_Lamp.jpg"
        caption="Dette er en bildetekst! :)"
        alt="Bildet viser no greier"
        size="full"
      />
      <Figure
        image="https://greekcitytimes.com/wp-content/uploads/2018/05/Pythagoros.jpg"
        caption="Dette er en bildetekst! :)"
        alt="Bildet viser no greier"
        size="full"
      />
    </div>
  </section>
</template>

<script>
import Figure from '@/components/Figure.vue'

export default {
  name: 'Gallery',
  components: {
    Figure
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

.gallery {
  width: 100%;
  background: $color-black;
  padding-top: 1rem;
  padding-bottom: 4rem;
  position: relative;

  height: 100vh;
  overflow-y: hidden;

  .inner {
    height: 102vh;
    display: flex;
    position: absolute;
    top: 2.6rem;
    left: 2rem;
    right: 0;

    overflow-x: scroll;
    -webkit-overflow-scrolling: touch;
  }

  .figure {
    margin: 0 2rem 1rem 0;
    height: 90vh;
    figure {
      height: 90vh;
      img {
        height: 90vh;
      }
    }
  }
}
</style>
