<template>
  <OneHome></OneHome>
</template>

<script>
import OneHome from "./components/OneHome.vue";

export default {
  name: "App",
  components: {
    OneHome,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
