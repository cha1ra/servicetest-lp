<template>
  <div>
    <v-app-bar
      color="grey lighten-5"
      fixed
    >
      <v-toolbar-items>
        <v-btn text to="#">
          Top
        </v-btn>
        <v-btn text to="#service">
          サービス内容
        </v-btn>
        <v-btn text>
          開始までの流れ
        </v-btn>
      </v-toolbar-items>

      <div class="flex-grow-1" />

      <v-btn rounded class="deep-orange font-weight-bold" dark large to="#form">
        相談する
      </v-btn>
    </v-app-bar>
  </div>
</template>
