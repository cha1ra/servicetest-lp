<template>
  <v-row no-gutters>
    <v-col>
      <div class="display-1 font-weight-bold text-center mb-4">
        よくあるご質問
      </div>
      <div class="text-center mb-4">
        お客様から多くいただく質問を掲載いたします。
      </div>
      <v-expansion-panels focusable>
        <v-expansion-panel
          v-for="question in questions"
          :key="question.id"
        >
          <v-expansion-panel-header>Q. {{ question.q }}</v-expansion-panel-header>
          <v-expansion-panel-content>A. {{ question.a }}</v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data () {
    return {
      questions: [
        {
          id: 1,
          q: '自分のアイディアが第三者に流出しないかが心配です。',
          a: 'サービスの利用を開始される際にNDA(秘密保持契約)を締結いたします。また、お借りするデータについては当社規定に基づき厳重に管理いたします。'
        },
        {
          id: 4,
          q: 'サービスとして提示されていること以外の事も頼みたいです。',
          a: '内容に応じて対応が可能です。まずは担当コンサルタントまでお問い合わせください。'
        },
        {
          id: 2,
          q: '費用はいつから発生しますか？',
          a: '無料の初回相談が終了した後、お見積もりを提示いたします。お見積もりに同意いただいて初めて料金が発生します。'
        },
        {
          id: 3,
          q: 'テスト終了後の運営についてもお手伝いいただきたいです。',
          a: '担当コンサルタントまでお問い合わせください。'
        }
      ]
    }
  }
}
</script>
