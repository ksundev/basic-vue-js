<template>
  <form action="">
    <div>
      <label for="userId">아이디:</label>
      <input id="userId" type="text" v-model="userId">
    </div>
    <div>
      <label for="password">비밀번호:</label>
      <input id="password" type="text" v-model="password">
    </div>
    <button type="submit">로그인</button>
  </form>
</template>

<script>
  export default {
    data() {
      return {
        userId: '',
        password: ''
      }
    },
  }
</script>

<style scoped>

</style>