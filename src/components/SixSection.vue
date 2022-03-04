<template>
  <div class="section-six py-5">
      <div class="container-fluid text-center">

        <!-- titolo -->
        <div class="text-capitalize fw-bold title">
            Latest News &amp; Our <span class="ms-green">Blog</span>
        </div>
        <div class="divider my-5"></div>
        <!-- fine titolo -->

        <!-- card 3 immagini -->
        <div class="row row-cols-3">
            <!-- componente card inserito - collegamento -->
            <SixSectionCard v-for="(card, i) in cardsData" :key="i" :cardData="card"/>
        </div>
        <!-- fine card 3 immagini -->

        <button class="ms-btn ms-btn-black me-4 mt-5">
                  VIEW ALL POST
        </button>

      </div>
  </div>
</template>

<script>

import SixSectionCard from './SixSectionCard.vue'

export default {
    name: "SixSection",
    components: {
        SixSectionCard
    },
    data() {
        return {
            cardsData: [
                {
                    img: 'serious-businesswoman-with-documents-talking-on-P9Q6LX6-1024.jpg',
                    data: 'May 24, 2018 •by Alex',
                    title: 'Marketing Ideas'
                },
                {
                    img: 'Businessman-at-the-desk-in-his-office-resting--1024x768.jpg',
                    data: 'May 24, 2018 •by Alex',
                    title: 'Rest During Working Hours'
                },
                {
                    img: 'simple-home-office-with-tree-PBXRXYB-large-1024x768.jpg',
                    data: 'May 24, 2018 •by Alex',
                    title: 'Develop Your Startup Idea'
                }
            ]
        }
    }

}
</script>

<style scoped lang="scss">
 @import '../style/general.scss';

    .section-six {
        background-color: #f9f9f9;

        .title{
        font-size: 50px;
        font-family: "Quicksand";
        font-weight: 600;
    }
    }

</style>