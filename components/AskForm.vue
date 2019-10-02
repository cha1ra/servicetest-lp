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
            <v-form ref="form" v-model="valid">
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
                    <v-btn color="deep-orange" dark block large @click="sendData">
                      送信
                    </v-btn>
                  </v-col>
                </v-row>
              </v-container>
            </v-form>
          </v-card>
          <v-snackbar
            v-model="snackbar"
          >
            送信が完了しました。担当より折り返しご連絡いたします。
            <v-btn
              color="pink"
              text
              @click="snackbar = false"
            >
              閉じる
            </v-btn>
          </v-snackbar>
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
    comment: '',
    snackbar: false
  }),
  methods: {
    sendData () {
      if (this.$refs.form.validate()) {
        console.log(this.name, this.email, this.phone, this.comment)

        const BASE_URL = process.env.WP_REST_API_BASE_URL
        const USER = process.env.WP_USER
        const PASSWORD = process.env.APPLICATION_PASSWORD

        // Base64に変換
        const TOKEN = window.btoa(`${USER}:${PASSWORD}`)
        const axiosConfig = {
          headers: {
            'Authorization': `Basic ${TOKEN}`,
            'Content-Type': 'application/x-www-form-urlencoded; charset=utf-8'
          }
        }

        // const params = {
        //   'yourName': this.name,
        //   'email': this.email,
        //   'phone': this.phone,
        //   'comment': this.comment
        // }

        const params = new URLSearchParams()
        params.append('yourName', this.name)
        params.append('email', this.email)
        params.append('phone', this.phone)
        params.append('comment', this.comment)

        this.$axios
          .post(BASE_URL + '/feedback/', params, axiosConfig)
          .then((response) => {
            console.log(response)
            this.responseData = response.data
          })
          .catch((error) => {
            console.log(error)
          })
        this.snackbar = true
      }
    }
  }
}
</script>
