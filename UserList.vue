<template>
  <div>
    <h1>Lista de usuarios</h1>
    <UserCard v-for="user in users" :key="user.id" :user="user" />
  </div>
</template>

<script>
import axios from "axios";
import UserCard from "./UserCard.vue";

export default {
  components: {
    UserCard,
  },
  data() {
    return {
      users: [],
    };
  },
  async mounted() {
    try {
      const response = await axios.get("https://dummyjson.com/users");
      this.users = response.data;
    } catch (error) {
      console.error("Error al cargar la lista de usuarios:", error);
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
