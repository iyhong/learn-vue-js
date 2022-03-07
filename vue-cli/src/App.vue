<template>
  <div>
    <p>
      {{ str }}
    </p>

    <AppHeader :str="str" @renew="renewStr" />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
export default {
  components: { AppHeader },
  data() {
    return {
      str: 'header',
    }
  },
  methods: {
    renewStr() {
      this.str = 'hi'
    },
  },
}
</script>

<style></style>
