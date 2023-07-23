<template>
  <div class="user-card-container">
    <div class="user-card">
      <div class="user-card-images">
        <img :src="user.image" alt="" />
      </div>
      <div class="user-card-text">
        <h2>{{ user?.firstName }} {{ user?.lastName }}</h2>
        <p>{{ user?.age }} años</p>
        <p>{{ user?.email }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    user: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style>
.user-card-container {
  display: inline-flex;
  flex-wrap: wrap;
  justify-content: space-around;
  width: 40%;
}

.user-card {
  margin: 20px;
  display: inline-block;
  border: 1px solid transparent;
  border-radius: 10px;
  background-color: antiquewhite;
  width: 500px;
}

.user-card-images {
  display: -webkit-inline-box;
}

.user-card-images > img {
  width: 180px;
  display: flex;
  margin-right: 10px;
}

.user-card-text {
  display: inline-block;
  text-align: initial;
}
p {
  font-size: 14px;
}

h2 {
  font-size: 20px;
}
h1 {
  text-align: left;
  padding-left: 150px;
}
</style>
