<template>
  <div class="section">
    <div class="container-fluid my-5 py-5">
      <div class="row my-5 g-0 align-items-center">
        <!-- inizio section sx -->
        <div class="col-5 px-4">
          <div class="text-capitalize fw-bold title">
            We are here to make your <span class="ms-green">website</span> look more <span class="ms-green">elegant</span> and stylish!
          </div>
          <div class="divider my-5"></div>
          <button class="ms-btn ms-btn-green">VIEW ALL</button>
        </div>
        <!-- fine section sx -->

        <!-- inizio section dx -->
        <div class="col-7">
          <div class="find row row-cols-2 g-5 m-0 p-0">

              <!-- con il ciclo for stampo ciò che voglio in base ai valori del mio array di oggetti che vado a richiamare -->
            <div v-for="(data, i) in findData" :key="i">
              <div class="card">
                <div class="background-hover"></div>
                <div class="card-text">
                    <!-- scorro le icone -->
                  <i :class="data.icon" class="mb-4"></i>
                  <!-- scorro titolo e testo sottostante -->
                  <h4 class="title fs-3 mb-2">{{data.title}}</h4>
                  <p class="my_fs text-secondary">{{data.text}}</p>
                </div>
              </div>
            </div>

          </div>
        </div>
        <!-- fine section dx-->
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name : 'SecondSection',
  data(){
    return{
        // array di oggetti da scorrere per ogni card
      findData : [
        {
          icon : 'fas fa-tachometer-alt fa-2xl',
          title : 'Speed optimization',
          text : 'Far far away, behind the word mountains, far from countries Vokalia Separated...'
        },
        {
          icon : 'fas fa-cloud fa-2xl',
          title : 'Cloud solution',
          text : 'Far far away, behind the word mountains, far from countries Vokalia Separated...'
        },
        {
          icon : 'fas fa-mobile-alt fa-2xl',
          title : 'Website design',
          text : 'Far far away, behind the word mountains, far from countries Vokalia Separated...'
        },
        {
          icon : 'fas fa-stopwatch fa-2xl',
          title : 'Online marketing',
          text : 'Far far away, behind the word mountains, far from countries Vokalia Separated...'
        },
      ]
    }
  }
}
</script>


<style scoped lang="scss">

@import '../style/general.scss';

  .section{
    
    .title{
      font-size: 50px;
      font-family: "Quicksand";
      font-weight: 600;
    }

    .find{
      position: relative;

      .card {
        box-shadow: 0 0 30px lightgray;
        border-radius: 20px;
        transition: all 0.5s;
        padding: 50px 70px;

        .my_fs {
            font-size: 14px;
        }

        // creo il box verde per l'effetto hover con opacità 0, quindi d-none
        .background-hover{
          position: absolute;
          top: 0;
          right: 0;
          bottom: 0;
          left: 0;
          border-radius: 20px;
          background-image: linear-gradient(to right, rgba(7, 217, 0, 0.8) , rgba(0, 219, 168, 0.8));
          transition: opacity 0.5s;
          opacity: 0;
        }

        .card-text{
          position: relative;
          z-index: 99;
        
          i{
            transition: all 0.5s;
            color: #00d9a6;
          }
        }
    
        &:hover{
          box-shadow: 5px 5px 20px  #00d9a656;
          color: #fff;
          cursor: pointer;
          
          // con hover d-block, metto opacità per visualizzare il box verde
          .background-hover{
            opacity: 1;
          }
    
          i {
            color: white;
          }
        }
      }
    }
    
  }
</style>