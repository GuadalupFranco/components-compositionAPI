<template>
  <div>{{ obj.counter }}</div>
</template>

<script> 
import { reactive, watch } from "vue"; // when using normal variables use ref

export default {
  setup() { 
    const obj = reactive({ counter: 0});
    setInterval(() => obj.counter++, 1000);

    watch(
      () => obj.counter, 
      (value, previus) => {
      console.log(value, previus);
    });

    return {
     obj, 
    };
  },
};
</script>