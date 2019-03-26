<template>
  <footer class="site-footer">
    <div class="flex">
      <div>
        <a href="https://www.hf.uio.no/ritmo/english">
          Forskningssenterets navn, avsender av artikkelen
        </a>
      </div>
      <div>
        <a href="https://uio.no">
          <img src="/uio-full.png" />
        </a>
      </div>
      <div>
        <p>
          Ansvarlig redaktør:<br />
          <a href="#">Navn Navnesen</a>
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style lang="scss" scoped>
@import '@/css/variables.scss';

.site-footer {
  width: 100%;
  padding: 5rem 1rem;
  background: $color-theme-dark;
  color: $color-white;

  text-align: center;
  font-family: $serif;
  line-height: 1.2;

  .flex {
    width: $width-xl;
    max-width: 100%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;

    div {
      width: 25%;
    }
  }

  p {
    line-height: 1.2;
    margin: 0 auto;
  }

  img {
    vertical-align: middle;
    padding: 0.5rem;
  }

  a {
    color: inherit;
    text-decoration: none;
  }

  @media (max-width: $media-m) {
    .flex {
      display: block;

      div {
        width: 100%;
        margin-bottom: 1rem;
      }
    }
  }
}
</style>

