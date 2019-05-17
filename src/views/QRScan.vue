<template>
  <v-content>
    <v-container fluid fill-height>
      <v-layout align-center justify-center>
        <v-flex xs12 sm8 md6>
          <v-card class="elevation-12">
            <v-toolbar dark color="primary">
              <v-toolbar-title>扫描二维码</v-toolbar-title>
            </v-toolbar>
            <v-card-text>
              <v-layout align-center justify-center>
              <v-btn v-if="!showScanner" flat @click="showScanner = true">打开相机</v-btn>
              <qrcode-stream v-else @decode="decoded"></qrcode-stream>
              </v-layout>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </v-content>
</template>

<script>
import { QrcodeStream } from 'vue-qrcode-reader'

export default {
  data () {
    return {
      showScanner: false
    }
  },
  components: {
    QrcodeStream
  },
  methods: {
    decoded(str){
      this.$router.push({
        name: 'show',
        params: {
          'id': str
        }
      })
    }
  }
}
</script>
