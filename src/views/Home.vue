<template>
  <div class="home">
    <h1>Welcome to the App!</h1>
    <template v-if="!this.$store.state.user">
      <div>
        To use this app you'll need to
        <router-link to="/login">
          Login
        </router-link>
        or
        <router-link to="/register">
          Register
        </router-link>
      </div>
    </template>
  </div>
</template>

<script>
import { authComputed } from '@/vuex/helpers.js'

export default {
  computed: {
    ...authComputed
  }
}
</script>
