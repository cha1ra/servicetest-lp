<template>
  <v-row no-gutters>
    <v-col>
      <div class="headline font-weight-bold text-center mb-2">
        ＼だからこそ／
      </div>
      <div class="display-1 font-weight-bold text-center mb-4">
        <span class="marker-cyan">
          <span class="ib">
            事前の検証が
          </span>
          <span class="ib">とても重要です</span>
        </span>
      </div>
      <v-row justify="center">
        <v-col
          cols="12"
          sm="11"
          md="10"
        >
          <v-img :src="require('@/static/intro.svg')" class="mb-8" />
        </v-col>
      </v-row>
      <v-row id="service">
        <v-col>
          <div class="display-1 font-weight-bold text-center mb-4">
            <span class="ib">
              弊社が提供する
            </span>
            <span class="ib">
              <span class="marker-cyan">主なサービス</span>について
            </span>
          </div>
        </v-col>
      </v-row>

      <v-row class="mb-8">
        <v-col
          v-for="s in services"
          :key="s.id"
          cols="12"
          sm="6"
          lg="3"
        >
          <v-card>
            <v-img :src="require(`@/static/f-${s.id}.png`)" />
            <v-card-title class="font-weight-bold">
              <span class="marker-cyan d-none d-sm-flex">
                {{ s.name }}
              </span>
              <span class="subtitle-1 font-weight-bold marker-cyan d-flex d-sm-none">
                {{ s.name }}
              </span>
            </v-card-title>
            <v-card-text>
              {{ s.desc }}
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
      <div class="title font-weight-bold text-center mb-8">
        ＼他にも様々なお手伝いをします／
      </div>
      <v-row justify="center">
        <v-col
          cols="12"
          md="10"
        >
          <v-list class="mb-8">
            <v-list-item v-for="o in options" :key="o.id" two-line>
              <v-list-item-content>
                <v-list-item-title>
                  {{ o.name }}
                </v-list-item-title>
                <v-list-item-subtitle>{{ o.desc }}</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data () {
    return {
      services: [
        {
          id: 1,
          name: 'ターゲット具体化コンサルティング',
          desc: 'ペルソナ・ジャベリンボード等のフレームワークを利用し、専任コンサルタントとともに貴方のサービスターゲット詳細を具体化します'
        },
        {
          id: 2,
          name: 'ターゲットへのインタビュー代行',
          desc: '平日に弊社スタッフがあなたに代わりインタビューを実施。結果をまとめ、ご報告いたします。'
        },
        {
          id: 3,
          name: '簡易なWebサイト作成',
          desc: '市場のニーズを調査するためのアンケートフォーム付きWebページ作成を代行。'
        },
        {
          id: 4,
          name: '事業計画書作成',
          desc: '目標金額, KPI を設定し、各数値を元に事業計画書を作成代行。'
        }
      ],
      options: [
        {
          id: 1,
          name: '広告代行',
          desc: 'テストページのインターネット広告ターゲティング・運用を実施。結果を基にコンサルティングを実施'
        },
        {
          id: 2,
          name: 'パワーポイント作成',
          desc: 'サービス概要資料 / 投資検討用資料 など、シチュエーションに応じたスライドを作成'
        },
        {
          id: 3,
          name: 'Webアプリケーション作成',
          desc: '会員登録、記事投稿などの本格運用に転用可能なWebサイトを作成'
        }
      ]
    }
  }
}
</script>
