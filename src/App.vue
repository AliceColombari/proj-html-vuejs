<template>
  <div id="app">
    <!-- importo tag file .vue collegati -->
    <MyHeader/>
    <MyMain/>
    
  </div>
</template>

<script>
// importo file .vue collegati
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';


export default {
  name: 'App',
  components: {
    // importo nome file .vue collegati
    MyHeader,
    MyMain
 
  }
}
</script>

<style lang="scss">

  // richiamo file scss general common
  @import './style/general.scss';
</style>
