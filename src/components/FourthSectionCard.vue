<template>
  <div class="section-card">
    <div class="pointer">
      <img :src="require(`../assets/image/${cardInfo.img}`)" alt="example" class="rounded rounded-3 w-100">
      <div class="layover rounded rounded-3 d-flex flex-column justify-content-end text-white pb-5">
        <div class="text">
          <h4 class="text-capitalize fs-5 fw-bold">
            {{cardInfo.title}} 
          </h4>
          <p class="text-uppercase">
            {{cardInfo.desc}}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name : 'FourthSectionCard',
  props : {
    cardInfo : Object,
  }
}
</script>


<style scoped lang="scss">

@import '../style/general.scss';

  .section-card{
    position: relative;
    transition: all 1s;

    &:hover{
      transform: scale(1.1);
      z-index: 9;
    }

    &:hover .layover{
      visibility: visible;
      opacity: 1;
    }

    .layover{
      z-index: 99;
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: linear-gradient(to right, rgba(7, 217, 0, 0.8) , rgba(0, 219, 168, 0.8));
      visibility: hidden;
      opacity: 0;
      transition: opacity 1s;

      .text{
        position: absolute;
        bottom: 10%;
        left: 10%;
        opacity: 0;

        &:hover{
            opacity: 1;
        }
      }
    }
  }
</style>