<template>
  <AppHeader :appTitle="message" @change="changeMessage"/>
</template>

<script>
  import AppHeader from './components/AppHeader.vue'

  export default {
    components: {
      "AppHeader": AppHeader
    },
    data() {
      return {
        message: "앱 헤더 컴포넌트"
      }
    },
    methods: {
      changeMessage() {
        this.message = "앱 헤더 컴포넌트 변경"
      }
    }
  }
</script>

<style scoped>

</style>