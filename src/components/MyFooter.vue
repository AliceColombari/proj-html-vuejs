<template>
  <footer>

    <!-- inizio footer top -->
    <div class="container-fluid">
      <div class="title-top row row-cols-4 my-5 py-5">

        <!-- inizio colonna 1 -->
        <div>
          <img src="../assets/image/cropped-Group-39-2x.png" class="mb-3">
          <div class="text-secondary">While the lovely valley teems with vapour around me, and the meridian sun strikes the upper surface of the impenetrable foliage of my trees.While the lovely valley teems with vapour around me.</div>
        </div>
        <!-- fine colonna 1 -->

        <!-- inzio colonna 2 -->
        <div>
          <div class="title">Quick links</div>
          <div class="divider my-3"></div>
          <ul>
            <li v-for="(link, i) in quickLinks" :key="i">
              <a :href="link.link"> {{link.text}} </a>
            </li>
          </ul>
        </div>
        <!-- fine colonna 2 -->

        <!-- inizio colonna 3 -->
        <div>
          <div class="title">Contact</div>
          <div class="divider my-3"></div>
          <div class="text-secondary">Patricia V. Amedee 4401 Waldeck Street Grepevine Nashville, TX 76051</div>
          <div class="my-3 text-secondary">info@yourdomain.com</div>
          <div class="text-secondary">+99 (0) 101 0000 888</div>
        </div>
        <!-- fine colonna 3 -->

        <!-- inizio colonna 4 -->
        <div>
          <div class="title">Location on map</div>
          <div class="divider my-3"></div>
          <img src="../assets/image/map.png" class="w-100">
        </div>
        <!-- fine colonna 4 -->

      </div>
    </div>
    <!-- fine footer top -->

    <!-- inizio footer bottom -->
    <div class="text-bottom d-flex justify-content-between align-items-center text-white px-5">
      <div class="left text-uppercase">
        &copy; 2020 Phlox business theme.
      </div>
      <div class="right">
        <i class="fab fa-facebook-f"></i>
        <i class="fab fa-twitter px-3"></i>
        <i class="fab fa-pinterest-p"></i>
      </div>
    </div>
    <!-- fine footer bottom -->

  </footer>
</template>


<script>
export default {
  name : 'MyFooter',
  data() {
    return {
      quickLinks : [
        {
          text : 'Careers',
          link : '#'
        },
        {
          text : 'News',
          link : '#'
        },
        {
          text : 'Terms of use',
          link : '#'
        },
        {
          text : 'Privacy Project',
          link : '#'
        },
        {
          text : 'About',
          link : '#'
        },
        {
          text : 'Contact',
          link : '#'
        }
      ]
    }
  }
}
</script>


<style scoped lang="scss">
  footer {
    .title-top {
        padding: 30px;
        font-family: "Quicksand";

      .title {
        text-transform: uppercase;
        font-size: 20px;
        font-weight: bold;
      }

      ul {
        list-style: none;
        padding: 0;

        li a {
          text-decoration: none;
          color: rgb(108, 117, 125);

          &:hover{
            color: #00d9a6;
            cursor: pointer;
          }
        }
      }
    }
    .text-bottom {
      height: 100px;
      background-image: linear-gradient(to right, rgb(54, 54, 54) , black);

      .right {
        margin: 0 10px;
      }
    }
  }
</style>