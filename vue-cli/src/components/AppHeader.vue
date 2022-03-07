<template>
  <header>
    <h1>{{ str }}</h1>
    <button @click="sendEvent">send</button>
  </header>
</template>

<script>
export default {
  props: ['str'],
  methods: {
    sendEvent() {
      this.$emit('renew')
    },
  },
}
</script>

<style></style>
