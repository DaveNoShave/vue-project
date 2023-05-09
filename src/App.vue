<template>
  <body>
  
    <div class="login-page">
      <img src="https://i.postimg.cc/gJXTPf3Q/bilen.png" alt="Bilen" />

      <form @submit.prevent="login">
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" required />

        <label for="password">Password:</label>
        <input type="password" id="password" v-model="password" required />

        <div>
          <label for="rememberMe">Remember me:</label>
          <input type="checkbox" id="rememberMe" v-model="rememberMe" />
        </div>

        <div class="button-container">
          <button type="submit">Login</button>
          <button
            type="button"
            @click="forgotPassword"
            class="forgot-password-button"
          >
            Forgot Password
          </button>
        </div>
      </form>
      <p v-if="error" class="error-message">{{ error }}</p>
    </div>
    <div class="footer">
      <div class="footer-content">
        <p>Contact us</p>
        <p>theniners@umu.se</p>
      </div>
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
  gap: 0.5rem;
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

.footer {
  background-color: #264653;
  width: 100%;
  position: fixed;
  bottom: 0;
  left: 0;
  padding: 1rem 0;
  display: flex;
  align-items: center;
  justify-content: center;
}

.footer-content {
  text-align: center;
}

.footer-content p {
  margin: 0;
  color: white;
  font-size: 1rem;
}

.footer-content p:first-child {
  margin-bottom: 0.25rem;
}

input[type="email"],
input[type="password"] {
  background-color: #E1F2FE;
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  outline: none;
  transition: 0.3s;
}

input[type="email"]:focus,
input[type="password"]:focus {
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
}

img {
  margin-right: 4rem;
}

  button {
    background-color: #E1F2FE;
    border: none;
    color: #333;
    padding: 0.25rem 0.5rem;
    border-radius: 20px;
    cursor: pointer;
    font-size: 0.9rem;
    transition: 0.3s;
  }

button:hover {
  background-color: #cde7fe;
}


.button-container {
    display: flex;
    gap: 0.5rem;
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
