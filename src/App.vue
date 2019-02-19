<template>
  <div id="app">
    <header class="site-header">
      <div class="logo"></div>
      <nav class="site-nav">
        <div class="menu" id="main-menu">
          <router-link to="/">Home</router-link>
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

  a {
    color: $color-white;
  }

  .menu-toggle {
    display: none;

    cursor: pointer;
    position: absolute;
    top: 1rem;
    right: 1rem;
  }

  @media (max-width: $media-s) {
    display: block;
    .menu-toggle {
      display: block;
    }
    .menu {
      width: 100%;
      margin: 2rem auto;
      text-align: center;

      display: none;
      &.visible {
        display: block;
      }
    }
  }
}

.site-main {
  margin-bottom: 8rem;
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
