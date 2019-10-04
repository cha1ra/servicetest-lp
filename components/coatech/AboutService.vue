<template>
  <v-container>
    <v-row>
      <v-col>
        <h2 class="headline text-center mb-4 font-weight-bold">
          <span class="ib">コードレビュー</span>
          <span class="ib">アウトソーシングサービス</span>
        </h2>
        <div class="text-center display-1 font-weight-bold mb-4">
          <img
            :src="require('@/static/coatech-logo.png')"
            style="max-width: 300px"
          >とは？
        </div>
        <div class="text-center mb-4">
          <p class="mb-1">
            CoaTechはコードレビューを実施するエンジニアと、
          </p>
          <p class="mb-1">
            コードレビューを希望する企業とをマッチングするオンラインプラットフォームです。
          </p>
        </div>

        <v-row justify="center">
          <v-col
            cols="12"
            sm="11"
            md="10"
          >
            <v-img :src="require('@/static/about-coatech.png')" />
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>
