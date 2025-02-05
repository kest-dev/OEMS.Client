<script lang="ts">
import axios from 'axios'

export default {
  data() {
    return {

    }
  },
  methods: {
    handleLogin() {
      axios.post('/api/login', {
        email: this.$refs.email.value,
        password: this.$refs.password.value
      })
      .then((response) => {
        console.log("Found user")
      })
      .catch((error) => {
        console.log("failed")
      })
    }
  }
}
</script>

<template>
  <main>
    <input type="text" ref="email">
    <input type="text" ref="password">
    <button @click="handleLogin">Login</button>
  </main>
</template>
