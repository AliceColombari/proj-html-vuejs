<template>
  <header>
    <!-- inizio header top-->
    <div class="header-top text-white">

      <!-- contenitore -->
      <div class="container-fluid d-flex justify-content-between align-items-center px-5">

        <!-- section sx --> 
        <div class="left">
          <i class="fas fa-phone"></i>
          <span class="px-3">(001) 88451234</span>
          <span>88451234</span>
        </div>

        <!-- section dx -->
        <div class="right">
          <i class="fab fa-facebook-f"></i>
          <i class="fab fa-twitter px-3"></i>
          <i class="fab fa-pinterest-p"></i>
        </div>

      </div>
      <!-- finecontenitore -->

    </div>
    <!-- fine header top-->

    <!-- inizio header bottom -->
    <div class="header-bottom">
      <!-- collego il file .vue creato per rendere dinamica la navbar -->
      <MyNavBar/>
    </div>
    <!-- fine header bottom -->

  </header>
</template>

<script>
import MyNavBar from './MyNavBar.vue';

export default {
  name: 'MyHeader',
  components: {
    // importo file navbar
    MyNavBar
  }
}
</script>

<style scoped lang="scss">

  header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 9999;
    box-shadow: 0 0 10px lightgray;

    .header-top {
      background-color: #3d3d3d;

      .container-fluid {
        height: 50px;
      }
    }

    .header-bottom {
      background-color: #fff;
    }
  }

</style>
