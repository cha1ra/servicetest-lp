<template>
  <v-container fluid class="pa-0">
    <header-image class="mb-8" />
    <about-service class="mb-8" />
    <problem />
    <solution class="mb-8" />

    <features class="mb-8" />
    <v-container fluid class="pa-0">
      <catch-copy />
    </v-container>
    <v-container>
      <ask-form class="pt-8 mb-8" />
    </v-container>
  </v-container>
</template>

<script>
import HeaderImage from '~/components/coatech/HeaderImage.vue'
import Features from '~/components/coatech/Features.vue'
import AskForm from '~/components/coatech/AskForm.vue'
import Problem from '~/components/coatech/Problem.vue'
import Solution from '~/components/coatech/Solution.vue'
import CatchCopy from '~/components/coatech/CatchCopy.vue'

import AboutService from '~/components/coatech/AboutService.vue'

export default {
  components: {
    HeaderImage,
    Features,
    AskForm,
    Problem,
    Solution,
    CatchCopy,
    AboutService
  },
  head () {
    return {
      title: 'CoaTech - コードレビューのアウトソーシングサービス',
      meta: [
        // `hid` は一意の識別子として使用されます。 `vmid` は動作しないので使わないでください。
        { hid: 'description', name: 'description', content: 'あなたのエンジニアスキルを使ってコードレビュアーとして活躍しませんか？ コードレビューアウトソーシングサービス CoaTech 事前登録受付中' }
      ],
      link: [
        { rel: 'icon', type: 'image/x-icon', href: '/coatech-favicon.ico' }
      ]
    }
  }
}
</script>
<style>
  .marker {
    background: linear-gradient(transparent 60%, #80CBC4 60%);
  }
  .marker-cyan {
    background: linear-gradient(transparent 60%, #80DEEA 60%);
  }
  .ib {
    display: inline-block;
  }
</style>
