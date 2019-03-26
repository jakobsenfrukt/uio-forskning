<template>
  <div class="home">
    <transition name="fade" appear>
      <Hero
        video="/video/monika.mp4"
        heading="Brenner for forskningskvalitet"
        subhead="Portrett av Monica Melby-Lervåg"
        id="intro"
      />
    </transition>
    <transition name="fadeup" appear>
      <Quote text="Å jobbe som praktiker har gjort meg til en annerledes forsker enn om jeg hadde begynt med forskning rett etter hovedfag." />
      <section class="text">
        <p class="lead">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
      </section>
    </transition>
    <section id="part1" class="text item">
      <p>Monica Melby-Lervåg fikk ikke den stipendiatstillinga hun søkte på da hun var ferdig med studiene i 2000. Det var kanskje likegreit. For i jobben ved PPT (pedagogisk-psykologisk tjeneste) i Nittedal og siden ved Torshov kompetansesenter, ble engasjementet for barn som strever på skolen for alvor vekka. Et engasjement som har prega hele forskergjerninga hennes siden. For det var mye spesialpedagogen savna da hun jobba i feltet.</p>
    </section>
    <section id="part1" class="text item">
      <h2>Nye perspektiver</h2>
      <p>For Melby-Lervåg ble jo etter hvert forsker. I 2004 søkte hun igjen på ei stipendiatstilling ved Institutt for spesialpedagogikk. Hun fikk den, og skrev doktorgradsavhandling om hvilke typer vansker som ligger til grunn for dysleksi.</p>
    </section>
    <FixedMedia
      image="/images/woman1.jpeg"
      :captions="[
        'Siden har hun vært her på Blindern, og i 2011 ble hun utnevnt til professor.',
        'Hun er forresten ikke bare på Blindern: I 2016 ble hun også utnevnt til professor ved Institutt for lærerutdanning og pedagogikk ved UiT – Norges arktiske universitet – i en 20 prosent stilling.',
        'Eiksmarka i Bærum og Tromsø, særlig når man har mann og to barn på 15 og 6 år. Så ukependling driver hun ikke med.'
      ]"
    />
    <section class="text item">
      <h3>&ndash; Hvordan ble du så interessert i språkutvikling?</h3>
      <p>&ndash; Jeg var egentlig ikke så interessert i det da jeg studerte – hovedoppgava mi handla om hukommelse hos synshemmede.  Men i PP-tjenesten jobba jeg mye med yngre barn, og innså at språk er utgangspunktet for all læring. Uten språk får barn problemer med samhandling med andre barn og med voksne. De får problemer med lesing og etter hvert med matematikk. Problemer med språkutvikling kan også være det første tegnet på store syndromer.</p>
    </section>
    <Figure
      image="/images/barn2.jpeg"
      caption="— Vansker med språket kan altså spre seg og gi store konsekvenser. Derfor er det viktig å bremse dem før det blir alt for alvorlig. De færreste kommer helt over vanskene, men de kan få en bedre skolehverdag med hjelp og tilrettelegging."
      alt="Bildet viser no greier"
      size="split full"
    />
    <section class="text item">
      <h2>Fattigdom påvirker læring</h2>
      <p>Når Melby-Lervåg skal trekke fram de forskningsprosjektene hun synes er de beste og viktigste i karrieren så langt, kommer hun opp med tre. Hun understreker at prosjektene er et resultat av teamarbeid, blant annet med ektemannen Arne Lervåg.</p>
    </section>
    <Quote text="Vi har lært mye av hverandre og utfyller hverandre på en veldig fin måte i prosjektene." />
    <section class="text item">
      <h3>Overskrift H3</h3>
      <p>Det tredje prosjektet hun vil trekke fram er nylig satt i gang. Det er et prosjekt med søkelys på matematikk og tallforståelse.</p>
    </section>
    <FixedGallery :media="gallery1" />
    <section class="text item">
      <h2>Et ungt forskningsfelt</h2>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
    </section>
    <MultiColumn :blocks="blocks1" />
    <section id="part3" class="text item background">
      <h2>Karriereløpsprogrammet for forskere</h2>
      <p>Det utdanningsvitenskapelige fakultet startet opp et karriereløpsprogram for fem utvalgte forskere i  2017. Disse er blant fakultetets mest fremragende forskere som er i en fase av karrieren hvor de holder på å bygge opp egne forskergrupper. Målet med karriereløpsprogram et er at kandidatene skal bygge karrieren sin slik at de er i best mulig posisjon til å nå opp i konkurrensen om prestisjetunge forskningsmidler fra blant annet Det europeiske forskningsrådet - ERC. ERC European Research Council støtter rein nysgjerrighetsdrevet forskning – altså grunnforskning, forskning som ikke er resultatavhengig. Deltakerne i programmet får to sjølvalgte mentorer. Programmet varer i 5 år.</p>
    </section>
    <Figure
      image="/images/barn3.jpeg"
      alt="Bildet viser no greier"
      size="full"
    />
    <section id="part2" class="text item">
      <h2>Overskrift H2 som kanskje går over to linjer</h2>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
    </section>
    <div class="facts item">
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
      image="/images/barn2.jpeg"
      caption="Dette er en bildetekst! :)"
      alt="Bildet viser no greier"
      size="column"
    />
    <Video
      video="/video/monika.mp4"
      caption="Dette er en bildetekst! :)"
      size="full"
    />
    <section id="part4" class="text item">
      <h2>Overskrift H2</h2>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
    </section>
    <div class="facts item">
      <div class="facts-inner background">
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
      image="/images/barn4.jpeg"
      caption="Dette er en bildetekst! :)"
      alt="Bildet viser no greier"
      size="column"
    />
    <section class="text item">
      <h3>Overskrift H3</h3>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
      <p>Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
    </section>
    <Quote text="Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since" />
    <section class="text item">
      <p>It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
    </section>
    <Figure
      image="/images/barn1.jpeg"
      caption="Dette er en lengre bildetekst som passer til en slik todelt bildekomponent. Det skal litt mer tekst til i denne for at det skal se fint ut."
      alt="Bildet viser no greier"
      size="split reverse quote"
    />
    <Video
      video="/video/monika.mp4"
      caption="Dette er en bildetekst! :)"
      size="column"
    />
    <div class="download item">
      <div class="inner">
        Last ned hele publikasjonen (PDF)
      </div>
    </div>
    <section id="end" class="text item background people">
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
import Quote from '@/components/Quote.vue'
import FixedMedia from '@/components/FixedMedia.vue'
import FixedGallery from '@/components/FixedGallery.vue'
import MultiColumn from '@/components/MultiColumn.vue'

export default {
  name: 'home',
  components: {
    Hero,
    Figure,
    Video,
    Quote,
    FixedMedia,
    FixedGallery,
    MultiColumn
  },
  data: function() {
    return {
      gallery1: [
        {
          image: '/images/barn1.jpeg',
          quote: 'Vi er interessert i å finne ut hvordan språk og språkutvikling påvirker matte og tall. Til det har vi rekruttert 300 5-åringer fra fire kommuner utafor Oslo. De skal følges til de er 18 år.'
        },
        {
          image: '/images/barn1.jpeg',
          caption: 'Forskerne skal se spesielt på kjønn og sosioøkonomiske forskjeller, og i starten skal barna bli kartlagt én gang i året. Etter hvert er tanken å slakke litt ned på kartleggingsintervallene.'
        },
        {
          image: '/images/barn1.jpeg',
          caption: 'Melby-Lervåg understreker at dette er en rein observasjonsstudie – de gjør ingen intervensjoner – så derfor er det heller ingen kontrollgruppe.',
          quote: 'Det er viktig med observasjonsstudier. Med utgangspunkt i slike store longitudinelle studier kan vi finne ut når og hvordan det skal interveneres. Dette kan igjen testes videre i tiltaksundersøkelser.'
        }
      ],
      blocks1: [
        {
          image: '/images/woman2.jpeg',
          heading: 'Et punkt med lenke',
          link: '#',
          text: 'Forskerne skal se spesielt på kjønn og sosioøkonomiske forskjeller, og i starten skal barna bli kartlagt én gang i året. Etter hvert er tanken å slakke litt ned på kartleggingsintervallene.'
        },
        {
          image: '/images/woman2.jpeg',
          heading: 'Et punkt med lenke',
          link: '#',
          text: 'Forskerne skal se spesielt på kjønn og sosioøkonomiske forskjeller, og i starten skal barna bli kartlagt én gang i året. Etter hvert er tanken å slakke litt ned på kartleggingsintervallene.'
        },
        {
          image: '/images/woman2.jpeg',
          heading: 'Et punkt med lenke',
          link: '#',
          text: 'Forskerne skal se spesielt på kjønn og sosioøkonomiske forskjeller, og i starten skal barna bli kartlagt én gang i året. Etter hvert er tanken å slakke litt ned på kartleggingsintervallene.'
        },
      ]
    }
  }
}
</script>

