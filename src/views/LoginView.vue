<script setup lang="ts">
import InputText from 'primevue/inputtext';
import Button from 'primevue/button';
import logo from '@/assets/logo.svg';
</script>

<template>
  <main>
    <div class="login">
      <h1>Login</h1>
      <form>
        <div>
          <label for="username">Username:</label>
          <InputText type="text" />
        </div>
        <div>
          <label for="password">Password:</label>
          <InputText type="password" />
        </div>
        <Button label="Submit" />
      </form>
      <p>Don't have an account? <a href="/register">Register here</a></p>
    </div>
    <div>
      <img :src="logo" alt="logo" width="80" height="80" />
    </div>
  </main>
</template>
