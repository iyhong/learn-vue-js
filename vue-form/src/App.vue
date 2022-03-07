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
    },
  },
}
</script>

<style></style>
