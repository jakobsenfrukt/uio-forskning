<template>
  <div id="app">
    <Header />
    <main class="site-main">
      <router-view/>
    </main>
    <Footer />
    <!--<div class="themeswitcher" @click="showThemeMenu = !showThemeMenu">+</div>
    <div class="thememenu" :class="{ visible: showThemeMenu }">
      hei
    </div>-->
  </div>
</template>

<script>
import Vue from 'vue';
import VueScrollTo from 'vue-scrollto';

import Footer from '@/components/Footer.vue'
import Header from '@/components/Header.vue'

Vue.use(VueScrollTo)

export default {
  components: {
    Header,
    Footer
  },
  data: function() {
    return {
      showThemeMenu: false,
    }
  },
  methods: {
    handleScroll: function() {
      this.fadeIn();
    },
    fadeIn: function() {
      const items = document.querySelectorAll('.item');
      for (const item of items) {
        if (item.getBoundingClientRect().top <= window.innerHeight * 0.8 && item.getBoundingClientRect().top > 0) {
          item.classList.add('inview');
        }
      }
    }
  },
  created() {
    window.addEventListener('scroll', this.handleScroll)
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="scss">
@import 'css/main.scss';

.themeswitcher {
  position: fixed;
  bottom: 0;
  left: 1rem;
  background: crimson;
  color: white;
  padding: 1rem;
  line-height: 1;
  cursor: pointer;
}
.thememenu {
  position: fixed;
  bottom: 0;
  left: 3rem;
  display: none;

  &.visible {
    display: block;
  }
}
</style>
