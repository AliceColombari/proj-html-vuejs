<template>
  <div class="h-100 slider-card">
      <div class="row h-100 w-100">
          <div class="col-6 d-flex flex-column justify-content-center px-5">
              <div class="text-uppercase ms-green fw-bold fs-7 mt-5"> 1 7 <span class="mx-1"></span> y e a r s <span class="mx-1"></span>o f <span class="mx-1"></span>e x p e r i e n c e</div>

              <div class="text-capitalize fw-bold title">
                  We are a <br>
                  Web Design <span class="ms-green">Agency</span>
              </div>

              <div class="divider my-2"></div>

              <p class="my-2"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Commodi dicta assumenda dolores quos culpa nesciunt soluta veniam cupiditate voluptatem temporibus, atque eaque repellat cum dolorum vero facere dolor, nihil laudantium.</p>


            <button class="ms-btn ms-btn-black me-4 mt-5">
                  READ MORE
            </button>

            <div class="social text-uppercase fs-6 fw-bold my-5">
                <a href="#">facebook</a>
                <span class="mx-3">-</span>
                <a href="#">instagram</a>
                <span class="mx-3">-</span>
                <a href="#">youtube</a>
                <span class="mx-3">-</span>
                <a href="#">twitter</a>
            </div>

          </div>

      </div>
  </div>
</template>

<script>
export default {
    name: "FirstSection"

}
</script>

<style scoped lang="scss">
 @import '../style/general.scss';

.slider-card {
    background-color: #f9f9f9;

    .title{
      font-size: 50px;
      font-family: "Quicksand";
    }

    a {
        text-decoration: none;
        color: #000;
    }

    .ms-btn {
        width: 200px;
    }

}


</style>