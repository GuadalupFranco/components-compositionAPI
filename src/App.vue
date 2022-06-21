<template>
  <div>{{ text }}</div>
  <div>{{ something }}</div>
</template>

<script>

import base from "@/mixins/base";

export default {
  name: "App",
  mixins:[base],
  components: {},
  data() {
    return {
      text: "Hello vue"
    };
  }, 
  beforeCreate(){
    console.log("beforeCreate", this.$data, this.$el);
  },
  created(){
    console.log("created", this.$data, this.$el);
  },
  beforeMount() {
    console.log("beforeMount", this.$data, this.$el);
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
