<script setup lang="ts">
import { ref } from "vue";
import { invoke } from "@tauri-apps/api/tauri";

const authMsg = ref("");
const username = ref("");
const password = ref("");

async function auth() {
  authMsg.value = await invoke("authenticate_user", { username: username.value, password: password.value });
}
</script>

<template>
  <form class="row" @submit.prevent="auth">
    <input id="greet-input" v-model="username" placeholder="Enter your username" />
    <input id="greet-input" type="password" v-model="password" placeholder="Enter your password" />
    <button type="submit">Login</button>
  </form>

  <p>{{ authMsg }}</p>
</template>
