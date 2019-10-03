<template>
  <v-container fluid class="pa-0">
    <v-img
      nuxt
      :src="require('@/static/consulting.jpg')"
    >
      <v-row
        align="center"
        justify="center"
        class="fill-height ma-0 bg-white"
      >
        <v-col>
          <div class="headline font-weight-bold text-center mb-2">
            ＼お任せください！／
          </div>
          <div class="headline font-weight-bold text-center mb-8">
            <span class="ib">
              その<span class="display-1 cyan--text font-weight-bold">悩みや課題</span>を
            </span>
            <span class="ib">
              <span class="display-1 cyan--text font-weight-bold">全て解決</span>します
            </span>
          </div>
          <v-container>
            <v-row>
              <v-col
                cols="12"
              >
                <v-card class="mb-4">
                  <v-list-item>
                    <v-list-item-avatar
                      size="80"
                      color="cyan"
                    >
                      <span class="font-weight-bold headline white--text">その1</span>
                    </v-list-item-avatar>
                    <v-list-item-content>
                      <v-list-item-title class="headline mb-1 no-ellipsis">
                        <span class="font-weight-bold marker-cyan">平日の営業時間帯</span>に貴方事業をサポート
                      </v-list-item-title>
                      <v-list-item-subtitle class="no-ellipsis">
                        平日の街頭インタビューなどを弊社スタッフが実施。仕事を続けながら貴方の事業を進めることができます。
                      </v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                </v-card>
                <v-card class="mb-4">
                  <v-list-item>
                    <v-list-item-avatar
                      size="80"
                      color="cyan"
                    >
                      <span class="font-weight-bold headline white--text">その2</span>
                    </v-list-item-avatar>
                    <v-list-item-content>
                      <v-list-item-title class="headline mb-1 no-ellipsis">
                        <span class="font-weight-bold marker-cyan">事業立ち上げ経験がある</span>コンサルタントが在籍
                      </v-list-item-title>
                      <v-list-item-subtitle class="no-ellipsis">
                        担当するコンサルタントは全員事業立ち上げ経験者。2社以上の事業立ち上げ経験があるコンサルタントも在籍しています。
                      </v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                </v-card>
                <v-card class="mb-4">
                  <v-list-item>
                    <v-list-item-avatar
                      size="80"
                      color="cyan"
                    >
                      <span class="font-weight-bold headline white--text">その3</span>
                    </v-list-item-avatar>
                    <v-list-item-content>
                      <v-list-item-title class="headline mb-1 no-ellipsis">
                        <span class="font-weight-bold marker-cyan">エンジニア・バックオフィス経験を持つスタッフ</span>が業務を代行
                      </v-list-item-title>
                      <v-list-item-subtitle class="no-ellipsis">
                        技術が必要な業務も、各担当スタッフが貴方をサポート。
                      </v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                </v-card>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
    </v-img>
  </v-container>
</template>
<style scoped>
  .bg-white{
    background-color: rgba(255,255,255,0.8);
  }
  .no-ellipsis{
    text-overflow: unset !important;
    white-space: normal !important;
  }
</style>
