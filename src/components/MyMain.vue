<template>
  <main>
      <FirstSection/>
      <SecondSection/>
      <ThirdSection/>
      <FourthSection/>
  </main>
</template>

<script>

import FirstSection from './FirstSection.vue';
import SecondSection from './SecondSection.vue';
import ThirdSection from './ThirdSection.vue';
import FourthSection from './FourthSection.vue';

export default {
    name: "MyMain",
    components: {
        FirstSection,
        SecondSection,
        ThirdSection,
        FourthSection

    }

}
</script>

<style lang="scss">

    main {
        margin-top: 150px;
    }
    
</style>