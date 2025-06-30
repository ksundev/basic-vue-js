<template>
  <form action="" @submit.prevent="submitForm">
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
import axios from 'axios'

  export default {
    data() {
      return {
        userId: '',
        password: ''
      }
    },
    methods: {
      submitForm() {
        const data = {
          userId: this.userId,
          password: this.password
        }
        axios.post('https://jsonplaceholder.typicode.com/users', data)
        .then(response => {
          console.log(response)
        })
      }
    }
  }
</script>

<style scoped>

</style>