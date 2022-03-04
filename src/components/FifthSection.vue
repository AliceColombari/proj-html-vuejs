<template>
  <div class="section-fifth">
    <div class="container-fluid my-5 py-5 overlay">

        <div class="ms-green virgolette text-center">“</div>

        <h1 class="text-light fst-italic fs-4 my-5 w-50 mx-auto text-center">When it comes to barbequing, there are two main schools of thought for the techniques that you can use. Freshly scrambled eggs with applewood smoked bacon - are amazing!</h1>
        <div class="client text-center"> 
            <img src="../assets/image/businesswoman-analysing-document-P8WSNMC-1024x820.jpg" class="mb-3">
            <h2 class="text-uppercase ms-green fs-5">Lissa Dublin</h2>
            <h6 class="text-light">Client</h6>
        </div>


    </div>
  </div>
</template>


<script>
export default {
  name : 'FifthSection'
}
</script>


<style scoped lang="scss">

    @import '../style/general.scss';

    .section-fifth {
        background-image: url('../assets/image/four-businesspeople-in-a-boardroom-with-paperwork-PC4V8H4.jpg');
        background-size: cover;
        background-position: center;

        .overlay {
            background-image: linear-gradient(to left, rgba(54, 54, 54, 0.8), rgba(0, 0, 0, 0.8));
        }

        .virgolette {
            font-size: 100px;
        }

        .client img {
            object-fit: cover;
            width: 100px;
            height: 100px;
            border-radius: 50%;
            border: 3px solid #fff;
        }
    }

</style>