<template>
  <div class="section-fourth">
    <div class="container-fluid my-5 py-5">

      <!-- inizio top section -->
      <div class="row align-items-end">

        <!-- inizio sx -->
        <div class="col-5 px-4">

          <div class="divider my-5"></div>

          <div class="title fw-bold">
            Our recent <span class="ms-green">web design</span> &amp; some examples of past <span class="ms-green">projects</span>
          </div>

          <div class="divider my-5"></div>

        </div>
        <!-- fine sx -->

        <!-- inizio dx -->
        <div class="col-7">
          <div class="text-secondary mb-5">
            Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.Separated they live in Bookmarksgrove.Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove.
          </div>
        </div>
        <!-- fine dx -->
      </div>
      <!-- fine top section -->

      <!-- inizio bottom section -->
      <div class="row row-cols-4 g-1 mb-5 bottom">
        <div v-for="(card,i) in cardData" :key="i">
          <FourthSectionCard :cardInfo="card"/>
        </div>
      </div>
      <!-- fine bottom section -->

      <!-- pulsante leggi ancora -->
      <div class="text-center">
        <button class="ms-btn ms-btn-green my-5">READ MORE</button>
      </div>

    </div>
  </div>
</template>

<script>

import FourthSectionCard from './FourthSectionCard.vue';

export default {
  name : 'FourthSection',
  components : {
    FourthSectionCard
  },
  data(){
    return{
      cardData : [
        {
          img : 'ina-soulis-227104-unsplash-1024x1024.jpg',
          title : 'The basket of flowers',
          desc : ' Branding - marketing '
        },
        {
          img : 'sunisa-misa-531163-unsplash-1024x1024.jpg',
          title : 'A famous ferris wheel ',
          desc : 'Marketing'
        },
        {
          img : '355H-1024x1024.jpg',
          title : 'Complementary colors',
          desc : 'Branding - Marketing'
        },
        {
          img : 'photo-1448932252197-d19750584e56-1024x1024.jpg',
          title : 'Business prestige',
          desc : 'Branding'
        },
        {
          img : 'business-competition-PB366D8-1024x1024.jpg',
          title : 'Colorful origami boats',
          desc : 'Branding - Marketing'
        },
        {
          img : 'cozy-sofa-in-living-room-PQR5AB9-1024x1024.jpg',
          title : 'Modern Couch',
          desc : 'Marketing'
        },
        {
          img : 'aa9a4539-PQGJ7HU-1024x1024.jpg',
          title : 'Hot air balloons',
          desc : 'Branding - Marketing'
        },
        {
          img : 'cody-davis-253928-unsplash-1024x1024.jpg',
          title : 'Make Difference',
          desc : 'Branding'
        },
      ]
    }
  }
}
</script>

<style scoped lang="scss">

@import '../style/general.scss';

  .section-fourth {
    overflow-x: hidden;

    .title {
      font-size: 50px;
      font-family: "Quicksand";
      font-weight: 600;
    }
  }
</style>