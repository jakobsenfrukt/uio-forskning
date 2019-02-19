<template>
  <div class="home">
    <Figure
      image="https://www.hf.uio.no/ritmo/bilder/forsidefoto-ritmo-970x400px.jpg"
      alt="Bildet viser no greier"
    />
    <section class="text">
      <h1>Overskrift H1</h1>
      <p class="lead">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
      <h2>Overskrift H2</h2>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
      <h3>Overskrift H3</h3>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
    </section>
    <Figure
      image="https://www.hf.uio.no/ritmo/bilder/forsidefoto-ritmo-970x400px.jpg"
      caption="Dette er en bildetekst! :)"
      alt="Bildet viser no greier"
    />
    <section class="text">
      <h2>Overskrift H2 som kanskje går over to linjer</h2>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import Figure from '@/components/Figure.vue'

export default {
  name: 'home',
  components: {
    Figure
  }
}
</script>
