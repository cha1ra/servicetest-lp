<template>
  <v-container fluid class="pa-0">
    <v-row no-gutter>
      <v-col class="pa-0">
        <v-parallax
          dark
          :src="require('@/static/mind.jpeg')"
        >
          <v-row
            align="center"
            justify="center"
          >
            <div style="text-align: center">
              <h4 class="headline mb-4 font-weight-bold">
                <span class="ib">自分のアイディア </span>
                <span class="ib">"仕事が忙しいから"と</span>
                <span class="ib">諦めていませんか？</span>
              </h4>
              <h1 class="pa-4 display-1 font-weight-bold mb-8 mark-full">
                <span class="ib">事業の</span>
                <span class="ib">アイディア検証</span>
                <span class="ib">お手伝いします</span>
              </h1>
              <v-btn rounded color="deep-orange font-weight-bold" dark x-large to="#form">
                まずは相談してみる(無料)
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
  background: linear-gradient(transparent 0%, #00BCD4 0%);
}
</style>
