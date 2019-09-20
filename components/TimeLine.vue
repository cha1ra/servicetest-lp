<template>
  <v-row>
    <v-col>
      <div class="display-1 font-weight-bold text-center mb-4">
        <span class="ib">
          サービス開始までの
        </span>
        <span class="ib">
          流れ
        </span>
      </div>
      <v-timeline :dense="$vuetify.breakpoint.smAndDown">
        <v-timeline-item
          color="deep-orange lighten-2"
          fill-dot
          right
        >
          <v-card>
            <v-card-title class="deep-orange lighten-2">
              <v-icon
                dark
                size="42"
                class="mr-4"
              >
                mdi-message
              </v-icon>
              <h2 class="display-1 white--text font-weight-light">
                お問い合わせ
              </h2>
            </v-card-title>
            <v-container>
              <v-row>
                <v-col cols="12">
                  まずは当ページのお問い合わせフォームからお申し込みをしてください。後日、弊社担当より連絡を差し上げます。<br>
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-timeline-item>
        <v-timeline-item
          color="deep-orange lighten-2"
          fill-dot
          left
        >
          <v-card>
            <v-card-title class="deep-orange lighten-2">
              <v-icon
                dark
                size="42"
                class="mr-4"
              >
                mdi-note-text
              </v-icon>
              <h2 class="display-1 white--text font-weight-light">
                ヒアリング
              </h2>
            </v-card-title>
            <v-container>
              <v-row>
                <v-col cols="12">
                  弊社担当コンサルタントが貴方の現状や実現したいサービスについてヒアリング。<br>
                  洗い出された課題を元に、貴方に最適な運用方法を探すお手伝いをいたします。
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-timeline-item>
        <v-timeline-item
          color="deep-orange lighten-2"
          fill-dot
          right
        >
          <v-card>
            <v-card-title class="deep-orange lighten-2">
              <v-icon
                dark
                size="42"
                class="mr-4"
              >
                mdi-timetable
              </v-icon>
              <h2 class="display-1 white--text font-weight-light">
                スケジュール提案
              </h2>
            </v-card-title>
            <v-container>
              <v-row>
                <v-col cols="12">
                  ヒアリング内容を基に実際のアクションプランとお見積もり金額を提示します。<br>
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-timeline-item>
        <v-timeline-item
          color="deep-orange lighten-2"
          fill-dot
          left
        >
          <v-card>
            <v-card-title class="deep-orange lighten-2">
              <v-icon
                dark
                size="42"
                class="mr-4"
              >
                mdi-check
              </v-icon>
              <h2 class="display-1 white--text font-weight-light">
                サービス開始
              </h2>
            </v-card-title>
            <v-container>
              <v-row>
                <v-col cols="12">
                  さあ、いよいよ行動開始です。アクションプランに沿ってテストを開始しましょう！
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-timeline-item>
      </v-timeline>
    </v-col>
  </v-row>
</template>
