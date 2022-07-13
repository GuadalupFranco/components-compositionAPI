<template>
  <MyHome firstName="Guadalupe" lastName="Franco" other="something"></MyHome>  
</template>

<script>
import MyHome from "./components/MyHome.vue";
import { provide } from "vue";

export default {
  name: "App",
  components: {
    MyHome,
  },
  setup() {
    provide("username", "frncorg");
  }
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
