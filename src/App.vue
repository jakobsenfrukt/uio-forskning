<template>
  <div id="app">
    <header id="header" class="site-header">
      <div class="logo">UiO</div>
      <nav class="site-nav">
        <div class="menu" id="main-menu">
          <ul>
            <!--<li><router-link to="/">Home</router-link></li>-->
            <h3>Overskrift H1</h3>
            <span class="subhead">RITMO - Centre for Interdisciplinary Studies in Rhythm, Time and Motion</span>
            <li><a href="#" v-scroll-to="{ el: '#intro', onStart: togglemenu }">Introduksjon</a></li>
            <li>
              <a href="#" v-scroll-to="{ el: '#part1', onStart: togglemenu }">Hva er RITMO?</a>
              <ul>
                <li><a href="#" v-scroll-to="{ el: '#part2', onStart: togglemenu }">Rytme</a></li>
                <li><a href="#" v-scroll-to="{ el: '#part3', onStart: togglemenu }">Tid</a></li>
                <li><a href="#" v-scroll-to="{ el: '#part4', onStart: togglemenu }">Bevegelse</a></li>
              </ul>
            </li>
            <li><a href="#" v-scroll-to="'#end'">Ansatte</a></li>
          </ul>
        </div>
        <div class="menu-toggle" @click="togglemenu()">
          <template v-if="showmenu">&times;</template>
          <template v-else>=</template>
        </div>
      </nav>
    </header>
    <main class="site-main">
      <router-view/>
    </main>
    <footer class="site-footer">
      <a href="#">Gå til uio.no</a>
    </footer>
  </div>
</template>

<script>
import Vue from 'vue';
import VueScrollTo from 'vue-scrollto';

Vue.use(VueScrollTo)

export default {
  data: function() {
    return {
      showmenu: false
    }
  },
  methods: {
    togglemenu: function() {
      document.getElementById('main-menu').classList.toggle('visible');
      this.showmenu = !this.showmenu;
    },
    handleScroll: function() {
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

.logo {
  font-family: $serif;
  padding-right: 0.6rem;
  position: relative;
  &:before, &:after {
    content: " ";
    display: block;
    width: 0.32rem;
    height: 0.32rem;
    border-radius: 50%;
    background: $color-red;
    position: absolute;
    top: 0.24rem;
    right: 0;
  }
  &:after {
    top: 0.7rem;
  }
}

.site-header {
  width: 100%;
  background: $color-black;
  color: $color-white;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 1rem;

  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  z-index: 200;


  a {
    color: $color-white;
  }

  .menu-toggle {
    display: block;

    cursor: pointer;
    position: absolute;
    top: 1rem;
    right: 1rem;
  }

  .menu {
    position: fixed;
    top: 3rem;
    right: 0;
    bottom: 0;
    z-index: 100;
    padding: 1rem;
    width: $width-xs;
    color: $color-white;
    background: $color-black;
    box-shadow: 0 0 1rem rgba(0, 0, 0, 0.6);

    transform: translateX($width-s);
    transition: transform .3s ease-in-out;

    &.visible {
      transform: translateX(0);
    }

    @media (max-width: $media-s) {
      width: 100%;
    }

    h3 {
      margin: 0;
      font-size: 2rem;
    }
    .subhead {
      font-size: $font-s;
      line-height: 1.2;
      display: block;
      margin: 0.5rem 0 2rem;
    }

    ul {
      list-style: none;
      font-size: 1.2rem;
      font-family: $sans-serif;

      @media (max-width: $media-s) {
        max-width: none;
        width: 100%;
        padding: 0;
      }
    }

    li {
      margin-left: 1rem;
      &:before {
        content: " ";
        display: inline-block;
        width: 0.4rem;
        height: 0.4rem;
        background: $color-red;
        border-radius: 50%;
        margin-right: 0.6rem;
      }
      

      ul {
        margin-top: 0.6rem;
        font-size: 1rem;
      }
    }

    a {
      color: $color-white;
      &:hover {
        text-decoration: underline;
      }
    }
  }
}

.site-footer {
  width: 100%;
  padding: 8rem 1rem 4rem;
  background: $color-black;
  color: $color-white;

  text-align: center;

  a {
    color: inherit;
    text-decoration: underline;
  }
}
</style>
