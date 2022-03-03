<template>
  <div>
      <div class="container-fluid d-flex justify-content-between align-items-center px-5">

          <img src="../assets/image/cropped-Group-39-2x.png" alt="">

          <nav>
              <ul class="m-0">
                  <!-- attraverso l'utilizo del ciclo for, stampo ciò che voglio n volte in base ai valori del mio array -->
                  <li v-for="(link, i) in navLinks" :key="i" class="d-inline-block mx-3">
                      <a href="#"
                      class="text-uppercase text-decoration-none"
                      :class="(activePage == i)">
                      {{link}}</a>
                  </li>
              </ul>
          </nav>

          <div class="d-flex align-items-center">
              <button class="ms-btn ms-btn-green me-4">
                  PURCHASE
              </button>
              
              <i class="fas fa-search ms-green pointer"></i>
          </div>

      </div>
  </div>
</template>

<script>
export default {
    name: 'MyNavBar',
    data() {
        return {
            // array da scorrere con l'uso del ciclo v-for
            navLinks: ['Home', 'About', 'Services', 'Showcase', 'Blog', 'Contact'],
            // numero da aggiungere per le pagine attive in riferimento
            activePage: 0,
        }
    }

}
</script>

<style scoped lang="scss">

.container-fluid {
        height: 100px;

        nav ul {
          list-style: none;

          a {
            color: #000;

            &:hover {
              color: grey;
            }
          }
        }
}
</style>