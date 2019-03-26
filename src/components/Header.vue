<template>
  <header id="header" class="site-header">
    <div class="logo"><img src="/uio-logo.svg" /></div>
    <nav class="site-nav">
      <div class="menu" :class="{ visible: showmenu }" id="main-menu">
        <ul>
          <!--<li><router-link to="/">Home</router-link></li>-->
          <h3>Overskrift H1</h3>
          <span class="subhead">Forskningssenterets navn: Avsender av artikkelen</span>
          <li><a href="#" v-scroll-to="{ el: '#intro', onStart: togglemenu }">Introduksjon</a></li>
          <li>
            <a href="#" v-scroll-to="{ el: '#part1', onStart: togglemenu }">Menypunkt</a>
            <ul>
              <li><a href="#" v-scroll-to="{ el: '#part2', onStart: togglemenu }">Undermenypunkt</a></li>
              <li><a href="#" v-scroll-to="{ el: '#part3', onStart: togglemenu }">Undermenypunkt</a></li>
              <li><a href="#" v-scroll-to="{ el: '#part4', onStart: togglemenu }">Undermenypunkt</a></li>
            </ul>
          </li>
          <li><a href="#" v-scroll-to="{ el: '#part1', onStart: togglemenu }">Menypunkt</a></li>
          <li><a href="#" v-scroll-to="{ el: '#part1', onStart: togglemenu }">Menypunkt</a></li>
          <li><a href="#" v-scroll-to="{ el: '#part1', onStart: togglemenu }">Menypunkt</a></li>
          <li><a href="#" v-scroll-to="'#end'">Ansatte</a></li>
        </ul>
      </div>
      <div class="menu-toggle" :class="{ open: showmenu }" @click="togglemenu()">
        <div class="burger-wrapper">
          <div class="burger"></div>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data: function() {
    return {
      showmenu: false
    }
  },
  methods: {
    togglemenu: function() {
      this.showmenu = !this.showmenu;
    },
    handleScrollMenu: function() {
      this.updateMenu();
    },
    updateMenu() {
      const chapters = document.querySelectorAll('.toc');
      for (const chapter of chapters) {
        if (chapter.getBoundingClientRect().top <= window.innerHeight * 0.5 || chapter.getBoundingClientRect().bottom < window.innerHeight * 0.5) {
          document.querySelector('.toc-inview').classList.remove('toc-inview');
          chapter.classList.add('toc-inview');
          const chapterId = chapter.getAttribute('id');
          const menu = document.querySelectorAll('#main-menu ul li a');
          for (const menuItem of menu) {
            if (menuItem.id === chapterId + '-link') {
              document.querySelector('.toc-link-active').classList.remove('toc-link-active');
              menuItem.classList.add('toc-link-active');
            }
          }
        }
      }
    }
  },
  created() {
    window.addEventListener('scroll', this.handleScrollMenu)
    this.updateMenu();
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScrollMenu)
  }
}
</script>

<style lang="scss">
@import '@/css/variables.scss';

.logo {
  font-family: $serif;
  padding-right: 0.6rem;
  position: relative;
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
    top: 1.5rem;
    right: 1rem;

    transition-timing-function: linear;
    transition-duration: .15s;
    transition-property: opacity,filter;

    .burger-wrapper {
      position: relative;
      width: 1.6rem;
      height: 1.6rem;
      display: block;

      .burger {
        transition-timing-function: cubic-bezier(.55,.055,.675,.19);
        transition-duration: 75ms;
        position: absolute;
        width: 1.6rem;
        height: 3px;
        transition-timing-function: ease;
        transition-duration: 0.2s;
        transition-property: transform;
        background: $color-white;

        &:before, &:after {
          display: block;
          content: "";
          position: absolute;
          width: 1.6rem;
          height: 3px;
          transition-timing-function: ease;
          transition-duration: 0.2s;
          transition-property: transform;
          background: $color-white;
        }
        &:before {
          transition: top 75ms ease .12s,opacity 75ms ease;
          top: -10px;
        }
        &:after {
          transition: bottom 75ms ease .12s,transform 75ms cubic-bezier(.55,.055,.675,.19);
          bottom: -10px;
        }
      }
    }

    &.open {
      .burger-wrapper {
        .burger {
          transition-delay: 0.06s;
          transition-timing-function: cubic-bezier(.215,.61,.355,1);
          transform: rotate(45deg);
          background: $color-white;

          &:before {
            top: 0;
            transition: top 75ms ease,opacity 75ms ease 0.16s;
            opacity: 0;
          }
          &:after {
            bottom: 0;
            transition: bottom 75ms ease,transform 75ms cubic-bezier(.215,.61,.355,1) .12s;
            transform: rotate(-90deg);
          }
        }
      }
    }

    &:hover {
      .burger-wrapper .burger {
          background: $color-theme;
          &:before, &:after {
            background: $color-theme;
          }
        }
    }
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
      line-height: 1.2;
      display: block;
      margin: 0.5rem 0.5rem 2rem 0;
      padding-bottom: 1rem;
      border-bottom: 1px solid $color-white;
      font-size: 0.95rem;
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

      ul {
        margin: 0.6rem 0 0.8rem;
        font-size: 1rem;
      }
    }

    a {
      color: $color-white;
      text-decoration: none;
      display: inline-block;
      &:before {
        content: " ";
        display: inline-block;
        width: 0.3rem;
        height: 0.3rem;
        vertical-align: middle;
        background: $color-theme;
        border-radius: 0.3rem;
        margin-right: 0.6rem;
      }
      &.toc-link-active {
        &:before {
          background: $color-theme;
        }
      }
      &:hover {
        text-decoration: underline;
      }
    }
  }
}
</style>
