<template>
  <div class="home">
    <Hero
      image="http://res.cloudinary.com/simpleview/image/upload/v1450121336/clients/norway/glacier-svalbard-norway_2-1_9bd1ba9d-535d-4bac-9861-cac5c04950dc.jpg"
      heading="Overskrift H1"
      id="intro"
    />
    <section id="part1" class="text">
      <p class="lead">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
      <h2>Overskrift H2</h2>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
      <Video
        video="https://www.youtube.com/embed/PKMQzkIiB0Y"
        caption="Dette er en bildetekst! :)"
        size="column"
      />
      <h3>Overskrift H3</h3>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
      <blockquote>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since.</blockquote>
    </section>
    <Figure
      image="https://www.hf.uio.no/ritmo/bilder/forsidefoto-ritmo-970x400px.jpg"
      caption="Dette er en bildetekst! :)"
      alt="Bildet viser no greier"
      size="full"
    />
    <section id="part2" class="text">
      <h2>Overskrift H2 som kanskje går over to linjer</h2>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
    </section>
    <Figure
      image="https://www.mn.uio.no/geo/english/research/news-and-events/news/2018/bilder/greenland-507px.jpg"
      caption="Dette er en bildetekst! :)"
      alt="Bildet viser no greier"
      size="column"
    />
    <section id="part3" class="text background">
      <h2>Overskrift H2</h2>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
    </section>
    <Video
      video="https://www.youtube.com/embed/PKMQzkIiB0Y"
      caption="Dette er en bildetekst! :)"
      size="full"
    />
    <section id="part4" class="text">
      <h2>Overskrift H2</h2>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
      <div class="facts">
        <div class="facts-inner">
          <h3>Dette er fakta</h3>
          <ul>
            <li>Lorem Ipsum is simply dummy text of the printing and typesetting industry.</li>
            <li>Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</li>
            <li>It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.</li>
            <li>It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</li>
          </ul>
        </div>
      </div>
      <Figure
        image="https://www.hf.uio.no/ritmo/bilder/forsidefoto-ritmo-970x400px.jpg"
        caption="Dette er en bildetekst! :)"
        alt="Bildet viser no greier"
        size="column"
      />
      <h3>Overskrift H3</h3>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
      <div class="download">
        <div class="inner">
          Last ned hele publikasjonen (PDF)
        </div>
      </div>
    </section>
    <section id="end" class="text background people">
      <h3>Ansatte</h3>
      <ul>
        <li>
          <img src="https://pbs.twimg.com/profile_images/941101314938949638/wc2T0MFY_400x400.jpg" />
          <h4 class="name">Navn Navnesen</h4>
          <p class="bio">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.</p>
        </li>
        <li>
          <img src="https://pbs.twimg.com/profile_images/941101314938949638/wc2T0MFY_400x400.jpg" />
          <h4 class="name">Navn Navnesen</h4>
          <p class="bio">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.</p>
        </li>
        <li>
          <img src="https://pbs.twimg.com/profile_images/941101314938949638/wc2T0MFY_400x400.jpg" />
          <h4 class="name">Navn Navnesen</h4>
          <p class="bio">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.</p>
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from '@/components/Hero.vue'
import Figure from '@/components/Figure.vue'
import Video from '@/components/Video.vue'

export default {
  name: 'home',
  components: {
    Hero,
    Figure,
    Video
  }
}
</script>
