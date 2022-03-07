<template>
  <div>
    <form @submit.prevent="submitForm">
      <div>
        <label for="userName">id: </label>
        <input id="userName" type="text" v-model="username" />
      </div>
      <div>
        <label for="password">pw: </label>
        <input id="password" type="password" v-model="password" />
      </div>
      <button type="submit">login</button>
    </form>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      username: '',
      password: '',
    }
  },
  methods: {
    submitForm() {
      console.log(this.username, this.password)
      axios
        .post('https://jsonplaceholder.typicode.com/users', {
          username: this.username,
          password: this.password,
        })
        .then((res) => {
          console.log(res)
        })
        .catch((err) => {
          console.log(err)
        })
    },
  },
}
</script>

<style></style>
