<template>
    <v-flex xs10 sm6 offset-sm3 offset-xs1>
      <v-card>
        <v-img
          :src="imgSrc"
        ></v-img>

        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0">沙漠</h3>
            <div>
              沙漠，主要是指地面完全被沙所覆盖、植物非常稀少、雨水稀少、空气干燥的荒芜地区。沙漠亦作“ 沙幕 ”，干旱缺水，植物稀少的地区。沙漠地域大多是沙滩或沙丘，沙下岩石也经常出现。有些沙漠是盐滩，完全没有草木。沙漠一般是风成地貌。沙漠里有时会有可贵的矿床，近代也发现了很多石油储藏。沙漠少有居民，资源开发也比较容易。沙漠气候干燥，它也是考古学家的乐居，可以找到很多人类的文物和更早的化石。
            </div>
          </div>
        </v-card-title>

        <v-card-actions>
          <v-btn flat color="orange">语音讲解</v-btn>
          <v-btn flat color="orange">观看视频</v-btn>
          <!-- <h1>{{this.$route.params.id}}</h1> -->
        </v-card-actions>
      </v-card>
    </v-flex>
</template>
<script>
var fly = require("flyio")
export default {
  data() {
    return {
      imgSrc: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
      itemName: '',
      itemText: '',
      imgAudioSrc: '',
      imgVideoSrc: '',
    }
  },
  created() {
    fly.get
  }
}
</script>

<style>
</style>