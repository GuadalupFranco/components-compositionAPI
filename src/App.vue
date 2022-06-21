<template>
  <div>{{ text }}</div>
</template>

<script>

export default {
  name: "App",
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
