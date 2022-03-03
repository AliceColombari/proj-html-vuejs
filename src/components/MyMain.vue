<template>
  <main>
      <FirstSection/>
      <SecondSection/>
  </main>
</template>

<script>

import FirstSection from './FirstSection.vue';
import SecondSection from './SecondSection.vue'

export default {
    name: "MyMain",
    components: {
        FirstSection,
        SecondSection

    }

}
</script>

<style lang="scss">

    main {
        margin-top: 150px;
    }
    
</style>