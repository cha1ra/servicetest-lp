<template>
  <v-container fluid class="pa-0">
    <v-container>
      <v-row>
        <v-col>
          <div class="text-center">
            <v-icon size="200" color="teal">
              mdi-chevron-down
            </v-icon>
          </div>
        </v-col>
      </v-row>
    </v-container>
    <v-img
      nuxt
      :src="require('@/static/solution.jpeg')"
    >
      <v-row
        align="center"
        justify="center"
        class="fill-height ma-0 bg-white"
      >
        <v-col>
          <div class="headline font-weight-bold text-center mb-2">
            ＼たったの３ステップ！／
          </div>
          <div class="headline font-weight-bold text-center mb-8">
            <span class="ib">
              <span class="display-1 teal--text font-weight-bold">CoaTech</span>を利用して
            </span>
            <span class="ib">
              <span class="display-1 teal--text font-weight-bold">自分のスキルを活用</span>
            </span>
            <span class="ib">
              しちゃいましょう！
            </span>
          </div>
          <div class="headline font-weight-bold text-center mb-2">
            ご利用までの流れ
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
                      color="teal"
                    >
                      <span class="font-weight-bold headline white--text">手順1</span>
                    </v-list-item-avatar>
                    <v-list-item-content>
                      <v-list-item-title class="headline mb-1 no-ellipsis">
                        <span class="font-weight-bold marker">基本情報</span>をCoaTechに登録
                      </v-list-item-title>
                      <v-list-item-subtitle class="no-ellipsis">
                        経験年数や言語・活動実績などのスキルや、週の稼働可能時間・希望時間単価など、ご自身に関わる情報を登録していただきます。
                      </v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                </v-card>
                <v-card class="mb-4">
                  <v-list-item>
                    <v-list-item-avatar
                      size="80"
                      color="teal"
                    >
                      <span class="font-weight-bold headline white--text">手順2</span>
                    </v-list-item-avatar>
                    <v-list-item-content>
                      <v-list-item-title class="headline mb-1 no-ellipsis">
                        <span class="font-weight-bold marker">コードレビュー希望企業</span>から連絡
                      </v-list-item-title>
                      <v-list-item-subtitle class="no-ellipsis">
                        コードレビューを希望する企業から問い合わせが入ると、お知らせを受信。具体的な契約の手続きが始まります。
                      </v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                </v-card>
                <v-card class="mb-4">
                  <v-list-item>
                    <v-list-item-avatar
                      size="80"
                      color="teal"
                    >
                      <span class="font-weight-bold headline white--text">手順3</span>
                    </v-list-item-avatar>
                    <v-list-item-content>
                      <v-list-item-title class="headline mb-1 no-ellipsis">
                        <span class="font-weight-bold marker">レビュー業務開始</span>
                      </v-list-item-title>
                      <v-list-item-subtitle class="no-ellipsis">
                        勤務条件が整ったらNDAを締結して、レビュー開始！プルリクエストが上がってきたらチェックし、コメントを残してください。
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
