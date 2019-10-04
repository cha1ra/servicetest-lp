<template>
  <v-container fluid class="pa-0">
    <v-row no-gutter>
      <v-col class="pa-0">
        <v-parallax
          dark
          :src="require('@/static/advice.jpeg')"
        >
          <v-row
            align="center"
            justify="center"
          >
            <div style="text-align: center">
              <h4 class="headline mb-4 font-weight-bold white--text">
                <span class="ib">実務経験を持つ</span>
                <span class="ib">エンジニアの皆様へ</span>
              </h4>
              <h1 class="pt-8 pb-8 pl-2 pr-2 ma-4  mb-8 display-2 font-weight-bold  black--text mark-full hidden-sm-and-down">
                <span class="teal--text display-3 font-weight-bold">コードレビュー</span>の副業<br>
                始めませんか？
              </h1>
              <h1 class="pt-8 pb-8 ma-4  mb-8 display-1 font-weight-bold  black--text mark-full hidden-md-and-up">
                <span class="teal--text display-2 font-weight-bold">コードレビュー</span>の副業<br>
                始めませんか？
              </h1>
              <v-btn rounded color="teal font-weight-bold" dark x-large to="#form">
                事前登録受付中
              </v-btn>
            </div>
          </v-row>
        </v-parallax>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
export default {

}
</script>
<style scoped>
.mark-full {
  background-color: rgba(255,255,255,0.8);
  border: 6px solid #009688;
}
</style>
