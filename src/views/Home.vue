<template>
<div>
  <v-toolbar app>
    <v-toolbar-side-icon></v-toolbar-side-icon>
    <v-toolbar-title>智慧博物馆</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items >
      <v-btn flat round @click="onScan">
        <v-icon>camera_alt</v-icon>
      </v-btn>
    </v-toolbar-items>
  </v-toolbar>
  <v-layout class="margin_top">
    <router-view></router-view>
  </v-layout>
</div>
</template>

<script>

export default {
  methods: {
    onScan() {
      this.$router.push('/scan')
    }
  }
}
</script>

<style scoped>
.margin_top {
  margin-top: 80px
}
</style>
