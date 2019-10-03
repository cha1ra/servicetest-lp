<template>
  <div class="bg-gra">
    <v-container>
      <v-row no-gutters>
        <v-col>
          <div class="headline font-weight-bold text-center mt-12 mb-12 white--text">
            <span class="ib">
              スタートアップ失敗の
            </span>
            <span class="ib">
              主な理由は
            </span><br>
            <span class="ib">
              <span class="display-1 font-weight-bold">製品のニーズが</span>
            </span>
            <span class="ib">
              <span class="display-1 font-weight-bold">なかった</span>から
            </span>
          </div>
          <v-img
            :src="require('@/static/why-fail.svg')"
          />
          <div class="text-right grey--text">
            出典:
            <a href="https://www.cbinsights.com/research/startup-failure-reasons-top/" target="_blank" class="grey--text">
              The Top 20 Reasons Startups Fail - CB Insights
            </a>
          </div>
          <div class="headline font-weight-bold text-center mt-12 mb-12 white--text">
            <span class="marker">
              <span class="ib">
                自分の思いつきだけを
              </span>
              <span class="ib">
                信じ込むことは
              </span>
              <span class="ib">
                <span class="display-1 font-weight-bold deep-orange--text">
                  非常に危険
                </span>
                です
              </span>
            </span>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<style scoped>
  .bg-gra{
    background: linear-gradient(90deg, #424242, #212121);
  }
</style>
