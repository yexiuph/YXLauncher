<script setup lang="ts">
import AuthenticateUser from "./components/auth/Authentication.vue";
</script>

<template>
  <div class="container">
    <h1>Welcome to YXGames!</h1>
    <AuthenticateUser />
  </div>
</template>

<style scoped>
.logo.vite:hover {
  filter: drop-shadow(0 0 2em #747bff);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #249b73);
}
</style>
