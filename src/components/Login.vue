<template>
  <div class="login-page">
    <h1>Iniciar sesión</h1>
    <form @submit.prevent="login">
      <label>
        Usuario:
        <input v-model="username" type="text" required />
      </label>
      <label>
        Contraseña:
        <input v-model="password" type="password" required />
      </label>
      <button type="submit">Iniciar sesión</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    login() {
      console.log(
        `Iniciando sesión con usuario: ${this.username} y contraseña: ${this.password}`
      );
    },
  },
};
</script>

<style>
.login-page {
  display: flex;
  flex-direction: column;
  align-items: center;
}

form {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #f2f2f2;
  padding: 20px;
  border-radius: 10px;
}

label {
  margin-top: 10px;
}

input[type="text"],
input[type="password"] {
  padding: 10px;
  font-size: 16px;
  margin-top: 10px;
}

button[type="submit"] {
  background-color: #4caf50;
  color: white;
  padding: 10px 20px;
  margin-top: 20px;
  border-radius: 10px;
  cursor: pointer;
}
</style>
