<template>
  <div class="slider position-relative">
    <div class="container-fluid m-0 px-0">

      <!-- @afterChange="loadnumber" -> funzione per per funzionare lo slider sui numeri, per cambio colore -->
      <!-- V-BIND stampa attributi, ci permette di inserire una variabile all'interno di un attributo di un tag -->
      <VueSlickCarousel v-bind="settings" @afterChange="loadnumber" ref="carousel">
        <!-- richiamo la card per visualizzare i risultati -->
        <!-- stampo a schermo i miei risultati - item in nomeArray -->
        <!-- item e chiave in nomeArray -->
        <FirstSectionCard
        v-for="(card, i) in cardInfo" :key="i"
        :cardInfomations="card"
        :activeClass="(i == index) ? 'active' : ''"
        />
      </VueSlickCarousel>

      <div class="counter-slider">
        <ul>
          <li 
          v-for="(counter, i) in cardInfo" 
          :key="i"
          @click="goToSlide(i)"
          role="button"
          :class="(index == i) ? 'active' : ''"> 
          <span v-if="i < 10">0</span>{{i}}</li>
        </ul>
      </div>

    </div>
  </div>
</template>


<script>

import FirstSectionCard from './FirstSectionCard.vue';
import VueSlickCarousel from 'vue-slick-carousel';
import 'vue-slick-carousel/dist/vue-slick-carousel.css';

export default {
  name : 'FirstSection',
  components : {
    FirstSectionCard,
    VueSlickCarousel
  },
  data(){
    return{
      index : 0,
      // funzionamento slider preso da "https://gs-shop.github.io/vue-slick-carousel/#/"
      settings : {
        accessibility : true,
        // eliminati pulsanti
        arrows : false,
        // funzionamento in auto
        autoplay : true,
        autoplaySpeed : 7000,
        infinite : true,
        initialSlide : 0,
        // pausa con hover
        pauseOnDotsHover : false,
        pauseOnFocus : false,
        pauseOnHover : true,
      },
      // ARRAY DI OGGETTI - struttura dati che contiene tutte le info necessarie - componente genitore
      cardInfo : [
        {
          TitleTop: 'We Are a',
          Subtitle: 'Web Design',
          SubtitleGreen: 'Agency',
          paragraf: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.Separated they live in Bookmarksgrove.',
          img: require('../assets/image/Group-36-2x.png')
        },
        {
          TitleTop: 'Analysis ',
          Subtitle: 'and competitive',
          SubtitleGreen: 'Benchmark',
          paragraf: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.Separated they live in Bookmarksgrove.',
          img: require('../assets/image/Group-40-2x.png')
        },
        {
          TitleTop: 'Custom',
          Subtitle: 'Web',
          SubtitleGreen: 'Development',
          paragraf: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.Separated they live in Bookmarksgrove.',
          img: require('../assets/image/Group-35-2x.png')
        }
      ]
    }
  },
  // METHODS - all'interno inserisco le funzioni
  methods : {
    loadnumber(loadedSlide){
      this.index = loadedSlide;
    },
    goToSlide(i){
      // ref consente di ottenere un riferimento diretto a un elemento DOM specifico, in questo caso a ref carousel
      this.$refs.carousel.goTo(i);
    }
  }
}
</script>


<style scoped lang="scss">
  .slider {
  margin-top: 150px;
  background-color: #f9f9f9;
  overflow: hidden;
  cursor: pointer;

  .counter-slider {
    position: absolute;
    bottom: 13%;
    left: 43%;
    transform: translateX(-50%);
    
    ul {
      background-image: linear-gradient(to right, rgb(54, 54, 54) , black);
      box-shadow: 5px 5px 20px  #00000056;
      border-radius: 100px;
      color: lightgray;
      list-style: none;
      margin: 0;
      padding: 0;
      
      li {
        padding: 8px 20px;
        margin: 5px;
        display: inline-block;
        border-radius: 100px;

        &.active {
          background-image: linear-gradient(to right, rgba(7, 217, 0, 0.8) , rgba(0, 219, 168, 0.8));
        }
      }
    }
  }
}
</style>