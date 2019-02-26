<template>
  <div id="app">
    <header class="site-header">
      <div class="logo"></div>
      <nav class="site-nav">
        <div class="menu" id="main-menu">
          <ul>
            <!--<li><router-link to="/">Home</router-link></li>-->
            <h3>Innhold</h3>
            <li><a href="#" v-scroll-to="'#intro'">Introduksjon</a></li>
            <li>
              <a href="#" v-scroll-to="'#part1'">Hva er RITMO?</a>
              <ul>
                <li><a href="#" v-scroll-to="'#part2'">Rytme</a></li>
                <li><a href="#" v-scroll-to="'#part3'">Tid</a></li>
                <li><a href="#" v-scroll-to="'#part4'">Bevegelse</a></li>
              </ul>
            </li>
            <li><a href="#" v-scroll-to="'#end'">Ansatte</a></li>
          </ul>
        </div>
        <div class="menu-toggle" @click="togglemenu()">
          <template v-if="showmenu">x</template>
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
    }
  }
}
</script>

<style lang="scss">
@import 'css/main.scss';

.logo {
  width: 1rem;
  height: 1rem;
  border-radius: 50%;
  background: $color-red;
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

    h3 {
      margin-top: 0;
    }

    ul {
      list-style: none;
      font-size: 1.2rem;
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

  @media (max-width: $media-s) {
    display: block;

    .menu {
      width: 100%;
      margin: 2rem auto;
      text-align: center;
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
