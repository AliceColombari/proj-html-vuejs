<template>
  <main>
      <FirstSection/>
      <SecondSection/>
      <ThirdSection/>
      <FourthSection/>
      <FifthSection/>
      <SixSection/>
  </main>
</template>

<script>

import FirstSection from './FirstSection.vue';
import SecondSection from './SecondSection.vue';
import ThirdSection from './ThirdSection.vue';
import FourthSection from './FourthSection.vue';
import FifthSection from './FifthSection.vue';
import SixSection from './SixSection.vue';

export default {
    name: "MyMain",
    components: {
        FirstSection,
        SecondSection,
        ThirdSection,
        FourthSection,
        FifthSection,
        SixSection

    }

}
</script>

<style lang="scss">

    main {
        margin-top: 150px;
    }
    
</style>