<template>
  <v-container fluid class="pa-0">
    <header-image class="mb-8" />
    <v-container>
      <problem class="mb-8" />
    </v-container>
    <solution class="mb-8" />

    <features />
    <v-container fluid class="pa-0">
      <catch-copy />
      <why-do-test class="mb-8" />
    </v-container>
    <v-container>
      <about-us class="mb-8" />
      <time-line class="mb-8" />
      <services class="mb-8" />
      <questions class="mb-12" />
      <ask-form class="pt-8 mb-8" />
    </v-container>
  </v-container>
</template>

<script>
import HeaderImage from '~/components/servicetest/HeaderImage.vue'
import Features from '~/components/servicetest/Features.vue'
import AskForm from '~/components/servicetest/AskForm.vue'
import WhyDoTest from '~/components/servicetest/WhyDoTest.vue'
import Problem from '~/components/servicetest/Problem.vue'
import Solution from '~/components/servicetest/Solution.vue'
import AboutUs from '~/components/servicetest/AboutUs.vue'
import Services from '~/components/servicetest/Services.vue'
import CatchCopy from '~/components/servicetest/CatchCopy.vue'
import Questions from '~/components/servicetest/Questions.vue'
import TimeLine from '~/components/servicetest/TimeLine.vue'

export default {
  components: {
    HeaderImage,
    Features,
    AskForm,
    WhyDoTest,
    Problem,
    Solution,
    AboutUs,
    Services,
    CatchCopy,
    Questions,
    TimeLine
  }
}
</script>
<style>
  .marker {
    background: linear-gradient(transparent 60%, #FFAB91 60%);
  }
  .marker-cyan {
    background: linear-gradient(transparent 60%, #80DEEA 60%);
  }
  .ib {
    display: inline-block;
  }
</style>
