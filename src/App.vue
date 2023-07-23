<template>
  <div id="app">
    <header>
      <img src="./assets/icon-256x256.avif" alt="Logo" class="logo" />
      <router-link to="/"
        ><button class="home-button">Inicio</button></router-link
      >
    </header>
    <UserList />
  </div>
</template>

<script>
import UserList from "./components/UserList.vue";

export default {
  components: {
    UserList,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

/* Estilos del logotipo y del botón */
.logo {
  width: 100px;
  height: auto;
  margin: 10px;
  display: block;
}

.home-button {
  position: absolute;
  top: 35px;
  right: 30px;
  padding: 10px 20px;
  background-color: #008cff;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.home-button:hover {
  background-color: #0056b3;
}
</style>
