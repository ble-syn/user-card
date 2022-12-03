<template>
  <NavBar />
  <UsersData />
</template>

<script>
import NavBar from "./components/NavBar.vue";
import UsersData from "./components/UsersData.vue";

export default {
  name: "app",
  components: {
    NavBar,
    UsersData,
  },
};
</script>

<style scoped></style>
