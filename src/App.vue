<template>
  <body>
    <div class="login-page">
      <img src="bilen.png" alt="Bilen" />
      <h1>Login</h1>
      <form @submit.prevent="login">
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" required />

        <label for="password">Password:</label>
        <input type="password" id="password" v-model="password" required />

        <div>
          <label for="rememberMe">Remember me:</label>
          <input type="checkbox" id="rememberMe" v-model="rememberMe" />
        </div>

        <button type="submit">Login</button>

        <button
          type="button"
          @click="forgotPassword"
          class="forgot-password-button"
        >
          Forgot Password
        </button>
      </form>
      <p v-if="error" class="error-message">{{ error }}</p>
    </div>
  </body>
</template>

<style>
body {
  background-color: red;
}
</style>

<script>
import { VButton } from 'vuestic-ui';

export default {
  name: 'MyComponent',
  components: {
    VButton,
  },
  data() {
    return {
      message: 'Hello, world!',
    };
  },
};
</script>
