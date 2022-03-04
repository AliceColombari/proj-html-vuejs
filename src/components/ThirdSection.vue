<template>
  <div class="section-third">
    <div class="container-fluid my-5 py-5">
      <div class="row g-0 align-items-center">

        <!-- inizio sx -->
        <div class="container-images col-7 left pe-5 position-relative">
          <div class="position-relative">
            <img src="../assets/image/busy-architect-PYVKWM4-1024x872.jpg" alt="business man">
            <div class="overlay"></div>
          </div>
          <img class="img-woman" src="../assets/image/businesswoman-analysing-document-P8WSNMC-1024x820.jpg" alt="business woman">
        </div>
        <!-- fine sx -->

        <!-- inizio dx -->
        <div class="col-5 p-5">
          <div class="title fw-bold">
            learn more about our <span class="ms-green">missions</span>
          </div>

          <div class="divider my-5"></div>

          <div class="text-secondary mb-3">Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.Separated they live in Bookmarksgrove.</div>

          <button class="ms-btn ms-btn-green mt-5">
            READ MORE
          </button>
        </div>
        <!-- fine dx -->
      </div>


    </div>
  </div>
</template>


<script>
export default {
  name : 'ThirdSection'
}
</script>


<style scoped lang="scss">

@import '../style/general.scss';

  .section-third {
    background-color: #f9f9f9;

    img {
      border-radius: 20px;
      box-shadow: 0 0 30px lightgray;
      width: 70%;
    }

    .title {
      font-size: 50px;
      font-family: "Quicksand";
      font-weight: 600;
    }
  }
  .container-images {
    left: -30px;
    margin-bottom: 120px;

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 70%;
      height: 100%;
      border-radius: 20px;
      background-image: linear-gradient(to right, rgba(7, 217, 0, 0.8) , rgba(0, 219, 168, 0.8));
    }

    .img-woman {
      position: absolute;
      top: 100px;
      left: 30%;
    }
  }
</style>