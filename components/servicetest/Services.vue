<template>
  <v-row no-gutters>
    <v-col>
      <div class="display-1 font-weight-bold text-center mb-4">
        お見積もり例
      </div>
      <div class="text-center mb-4">
        <p class="mb-1">
          <span class="ib">
            選択いただいたオプションによって
          </span>
          <span class="ib">
            料金は変動します
          </span>
        </p>
      </div>

      <v-row justify="center">
        <v-col
          cols="12"
          sm="11"
          md="8"
        >
          <v-card>
            <v-card-text class="black--text">
              <v-row v-for="item in items" :key="item.id" no-gutters>
                <v-col class="mb-2">
                  <div class="subtitle-1">
                    <span class="ib">
                      {{ item.name }}
                    </span>
                    <span class="ib">
                      ... {{ item.price }}
                    </span>
                  </div>
                </v-col>
              </v-row>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data () {
    return {
      items: [
        {
          id: 1,
          name: 'ターゲット具体化コンサルティング',
          price: '50,000 円'
        },
        {
          id: 2,
          name: 'ターゲットへのインタビュー代行',
          price: '1,000 円 / 人'
        },
        {
          id: 3,
          name: '仮説検証用Webテストサイト作成',
          price: '100,000 円 〜    '
        },
        {
          id: 4,
          name: '事業計画書作成',
          price: '30,000 円 〜   '
        }
      ]
    }
  }
}
</script>
