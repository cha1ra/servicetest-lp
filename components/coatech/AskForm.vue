<template>
  <v-row id="form" no-gutters>
    <v-col>
      <div class="headline text-center">
        ＼事前登録受付中／
      </div>
      <div class="display-1 font-weight-bold text-center mb-4">
        レビュアー登録申請
      </div>

      <div class="text-center mb-4">
        <p class="mb-1">
          現在CoaTechは事前登録受付中です。
        </p>
        <p class="mb-1">
          サービスがリリースされ次第、改めて本登録のご案内をお送りします。
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
                      label="現在のご職業"
                      :rules="phoneRules"
                      required
                      outlined
                      placeholder="例) アプリケーションエンジニア, サーバサイドエンジニア ..."
                    />
                    <v-textarea
                      v-model="
                        comment"
                      outlined
                      name="input-7-4"
                      label="エンジニアとしての経験"
                      placeholder="経験年数・経験言語などを記入してください"
                    />
                    <v-btn color="teal" dark block large @click="sendData">
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
            送信が完了しました。本登録が開始次第、改めてご案内いたします。
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
