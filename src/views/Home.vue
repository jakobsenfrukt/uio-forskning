<template>
  <div class="home">
    <transition name="fade" appear>
      <Hero
        image="http://res.cloudinary.com/simpleview/image/upload/v1450121336/clients/norway/glacier-svalbard-norway_2-1_9bd1ba9d-535d-4bac-9861-cac5c04950dc.jpg"
        heading="Overskrift H1"
        id="intro"
      />
    </transition>
    <transition name="fadeup" appear>
      <section class="text">
        <p class="lead">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
      </section>
    </transition>
    <section id="part1" class="text">
      <h2>Overskrift H2</h2>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
      <Video
        video="https://www.youtube.com/embed/PKMQzkIiB0Y"
        caption="Dette er en bildetekst! :)"
        size="column"
      />
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
      <p>It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
      <Figure
        image="https://media.gadventures.com/media-server/cache/c6/2e/c62e5721fef11ef37d6c0815821c7b25.jpg"
        caption="Dette er en lengre bildetekst som passer til en slik todelt bildekomponent. Det skal litt mer tekst til i denne for at det skal se fint ut."
        alt="Bildet viser no greier"
        size="split"
      />
      <h3>Overskrift H3</h3>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
      <Figure
        image="https://storage.googleapis.com/ahead4-thegreatprojects/uploads/85da00b6ade6c2208bebb586d13f86c5.jpg"
        caption="Dette er en lengre bildetekst som passer til en slik todelt bildekomponent. Det skal litt mer tekst til i denne for at det skal se fint ut."
        alt="Bildet viser no greier"
        size="split reverse quote"
      />
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
    </section>
    <Figure
      image="https://media.gadventures.com/media-server/cache/c6/2e/c62e5721fef11ef37d6c0815821c7b25.jpg"
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
      <p>It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
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
        image="https://images.theconversation.com/files/134262/original/image-20160816-12998-tf916v.jpg?ixlib=rb-1.1.0&q=45&auto=format&w=926&fit=clip"
        caption="Dette er en bildetekst! :)"
        alt="Bildet viser no greier"
        size="column"
      />
      <h3>Overskrift H3</h3>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
      <p>Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
      <blockquote>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since.</blockquote>
      <p>It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
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

