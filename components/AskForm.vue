<template>
  <v-row id="form" no-gutters>
    <v-col>
      <div class="headline text-center">
        ＼まずは無料相談から／
      </div>
      <div class="display-1 font-weight-bold text-center mb-4">
        お問い合わせ窓口
      </div>

      <div class="text-center mb-4">
        <p class="mb-1">
          まずは気軽にお問い合わせください。
        </p>
        <p class="mb-1">
          後日担当スタッフよりご連絡差し上げます。
        </p>
      </div>
      <v-row no-gutters justify="center">
        <v-col
          cols="12"
          sm="10"
          md="10"
        >
          <v-card>
            <v-form v-model="valid">
              <v-container>
                <v-row>
                  <v-col>
                    <v-text-field
                      v-model="name"
                      :rules="nameRules"
                      label="お名前"
                      required
                      outlined
                      placeholder="例) 山田 太郎"
                    />
                    <v-text-field
                      v-model="email"
                      :rules="emailRules"
                      label="メールアドレス"
                      required
                      outlined
                      placeholder="例) taroyamada@proglearn.com"
                    />
                    <v-text-field
                      v-model="phone"
                      label="電話番号"
                      :rules="phoneRules"
                      required
                      outlined
                      placeholder="例) 000-0000-0000"
                    />
                    <v-textarea
                      v-model="comment"
                      outlined
                      name="input-7-4"
                      label="コメント(任意)"
                      placeholder="疑問点・お聞きしたいことなどございましたら記載ください"
                    />
                    <v-btn color="deep-orange" dark block large>
                      送信
                    </v-btn>
                  </v-col>
                </v-row>
              </v-container>
            </v-form>
          </v-card>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data: () => ({
    valid: false,
    name: '',
    nameRules: [
      v => !!v || '名前を入力してください'
    ],
    email: '',
    emailRules: [
      v => !!v || 'Eメールを入力してください',
      v => /.+@.+/.test(v) || '有効なEメールを入力してください'
    ],
    phone: '',
    phoneRules: [
      v => !!v || '電話番号を入力してください'
    ],
    comment: ''
  })
}
</script>
