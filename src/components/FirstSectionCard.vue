<template>
  <div class="h-100 slider-card">

    <div class="row h-100 ps-5 position-relative overflow-hidden" :class="activeClass">
      <!-- lato sx - text -->
      <div class="col-6 altezza d-flex flex-column justify-content-center">
        
        <div class="experience text-uppercase position-relative ms-green fw-bold fs-5">17 years of experience</div>

        <!-- titolo diviso in due sezioni -->
        <!-- aggiungo attributi in base a quante sono le variabili di cui ho bisogno -->
        <!-- per poter ricevere info dal genitore, il componente figlio deve dichiarare tutte le variabili -->
        <div class="title fw-bold">
          <div>{{cardInfomations.TitleTop}}</div>
          <div>
            {{cardInfomations.Subtitle}} 
            <span class="ms-green">{{cardInfomations.SubtitleGreen}}</span>
          </div> 
        </div>

        
        <div class="divider my-5"></div>

        <!-- paragrafo -->
        <p class="card-infos">{{cardInfomations.paragraf}}</p>

        
        <div class="read-more my-5">
          <button class="ms-btn ms-btn-black">
            READ MORE
          </button>
        </div>

        <!-- link ai social -->
        <div class="social text-uppercase fs-6 fw-bold mt-5">
          <a href="#">Facebook</a>
          <span class="mx-3">-</span>
          <a href="#">Instagram</a>
          <span class="mx-3">-</span>
          <a href="#">Youtube</a>
          <span class="mx-3">-</span>
          <a href="#">Twitter</a>
        </div>
      </div>

      <!-- lato dx - immagine -->
      <img :src="cardInfomations.img" alt="img slider" class="slider-img">
    </div>

  </div>
</template>


<script>
export default {
  name : 'FirstSectionCard',
  // PROPS per passare dati da un componente genitore ad uno figlio
  // props come oggetto indicato il nome e anche che cosa sono
  // props come array di stringhe, contiene il nome delle variabili che il componente riceve
  props : {
    'cardInfomations' : Object,
    'activeClass' : String
  }
}
</script>


<style lang="scss">
  .slider-card {

    .experience {
      letter-spacing: 15px;
    }

    .title {
      font-size: 50px;
      font-family: "Quicksand";
      font-weight: 600;
      position: relative;
      z-index: 99;
      opacity: 1;
    }
  
    .card-infos {
      position: relative;
      z-index: 99;
      opacity: 1;
    } 

    .read-more button {
      position: relative;
      z-index: 99;
    }
  
    .slider-img {
      position: absolute;
      top: 50%;
      left: 80%;
      transform: translate(-50%, -50%);
      width: 75%;
      z-index: 9;
    }

    .altezza{
    height: 80vh;
    }

    .social {
      a {
        color: black;
        text-decoration: none;

        &:hover {
          color: #00d9a6;
          cursor: pointer;
        }
      }
    }
  }

</style>