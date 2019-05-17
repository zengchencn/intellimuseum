<template>
  <v-app>
    <router-view/>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      //
    }
  },
  created() {
    this.$router.replace({
      name: 'home',
      params: {
        id: 12345
      }
    })
  }
}
</script>
