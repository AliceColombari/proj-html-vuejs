<template>
  <div id="app">
    <!-- importo tag file .vue collegati -->
    <MyHeader/>
  </div>
</template>

<script>
// importo file .vue collegati
import MyHeader from './components/MyHeader.vue'

export default {
  name: 'App',
  components: {
    // importo nome file .vue collegati
    MyHeader,
  }
}
</script>

<style lang="scss">

  // richiamo file scss general common
  @import './style/general.scss';
</style>
