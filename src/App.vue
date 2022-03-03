<template>
  <div id="app" class="container text-center">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1 class="debug">Prova debug font quicksand</h1>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss">
  @import './style/general.scss';

  .debug {
    font-family: "quicksand";
  }
</style>
