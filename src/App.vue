<template>
  <body>
    <div class="login-page">
      <img
        src="https://github.com/DaveNoShave/vue-project/blob/571ea1be99a4e0aae12e66d45eaef41cf9fdb49e/src/bilen.png"
        alt="Bilen"
      />
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
  background-color: #2a9d8f;
  margin: 0;
  font-family: Arial, sans-serif;
}

.login-page {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  gap: 1rem;
}

form {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

form > div {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.error-message {
  color: red;
  font-size: 0.9rem;
  font-weight: bold;
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
