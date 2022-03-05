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

        <button class="ms-btn ms-btn-black me-4 my-5">
                  VIEW ALL POST
        </button>

      </div>

      <!-- box colorate -->
      <div class="container-fluid">
          <div class="color-box text-white m-3 text-center my-5">
                <!-- box sx -->
                <div class="left">
                    <div class="text-secondary">Are You Ready?</div>
                    <div class="fs-1 fw-bold">Start a New Project</div>
                    <div class="inserisci-email mt-5">
                        <input type="text" placeholder="Enter Your Email Address">
                        <button>
                        SUBMIT
                        </button>
                    </div>
                </div>
                <!-- fine box sx -->
                <!-- box dx -->
                <div class="right">
                    <div class="text-secondary">What Are you Waiting for?</div>
                    <div class="fs-1 fw-bold">Let's Talk About Work</div>
                    
                        <button class="ms-btn ms-btn-black me-4 mt-5">
                        START NOW
                        </button>
                    
                </div>
                <!-- fine box dx -->
            </div>
      </div>

      <!-- sponsor -->
      <div class="container-fluid">
          <div class="sponsor d-flex my-5">
              <img src="../assets/image/client-1-2x.png" alt="">
              <img src="../assets/image/client-9-2x.png" alt="">
              <img src="../assets/image/client-7-2x.png" alt="">
              <img src="../assets/image/client-3-2x.png" alt="">
              <img src="../assets/image/client-4-2x.png" alt="">
              <img src="../assets/image/client-5-2x.png" alt="">
          </div>
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

        .color-box {
            display: flex;
            justify-content: space-between;

            .left,
            .right {
                border-radius: 20px;
                padding: 50px 0px;
                width: 45%;
                font-family: "Quicksand";
            }

            .left {
                background-image: linear-gradient(to right, rgb(54, 54, 54), black);

                .inserisci-email {
                    width: 70%;
                    margin: 0 auto;
                    background-image: linear-gradient(to right, rgb(73, 73, 73) , rgb(53, 53, 53));
                    border: none;
                    border-radius: 100px;

                    input {
                        padding: 10px 20px;
                        background-color: unset;
                        border: none;
                        width: 70%;
                        outline: none;
                        float: left;
                    }

                    button {
                        padding: 10px 20px;
                        background-color: unset;
                        border: none;
                        color: gray;
                        float: right;
                    }
                }

                .inserisci-email::after {
                    content: "";
                    display: table;
                    clear: both;
                }

            }

            .right {
                background-image: linear-gradient(to right, rgba(7, 217, 0, 0.8) , rgba(0, 219, 168, 0.8));
            }
        }

        .sponsor {
            align-content: center;
            justify-content: space-around;
            align-items: center;

            img {
                width: 100px;
                object-fit: cover;
            }
        }

    }

</style>