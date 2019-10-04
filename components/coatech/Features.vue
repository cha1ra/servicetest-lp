<template>
  <v-row no-gutters>
    <v-col class="text-center">
      <div class="headline font-weight-bold mb-8 black--text">
        <span class="ib">手続きや実際の業務は</span>

        <span class="display-1 font-weight-bold teal--text">
          <span class="ib">全てオンライン上で</span>
          <span class="ib">
            完結します！
          </span>
        </span>
      </div>
      <v-container>
        <p>
          <span class="ib">
            レビューを希望する企業とは
          </span>
          <span class="ib">
            CoaTechのシステムを通じてマッチング。
          </span>
        </p>
        <p>
          <span class="ib">
            実際の業務もGitHubなどから送られてくる
          </span>
          <span class="ib">
            プルリクエストにコメントをしていただく事です。
          </span>
        </p>
        <p>
          <span class="ib">
            また、NDAなどの煩雑な事務手続きも弊社がサポート。
          </span>
          <span class="ib">
            リモートでの快適な勤務を実現します。
          </span>
        </p>
      </v-container>
      <v-row justify="center">
        <v-col
          cols="11"
          sm="10"
          md="6"
        >
          <v-img :src="require('@/static/pullrequest.png')" />
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>
<script>
export default {

}
</script>
