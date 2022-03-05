<template>
  <div id="app">
    <!-- importo tag file .vue collegati -->
    <MyHeader/>
    <MyMain/>
    <MyFooter/>
    <MyChatBtn/>
    
  </div>
</template>

<script>
// importo file .vue collegati
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
import MyFooter from './components/MyFooter.vue';
import MyChatBtn from './components/MyChatBtn.vue';


export default {
  name: 'App',
  components: {
    // importo nome file .vue collegati
    MyHeader,
    MyMain,
    MyFooter,
    MyChatBtn
 
  }
}
</script>

<style lang="scss">

  // richiamo file scss general common
  @import './style/general.scss';
</style>
