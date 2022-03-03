<template>
  <main>
      <FirstSection/>
  </main>
</template>

<script>

import FirstSection from './FirstSection.vue';

export default {
    name: "MyMain",
    components: {
        FirstSection,

    }

}
</script>

<style lang="scss">

    main {
        margin-top: 150px;
    }
    
</style>