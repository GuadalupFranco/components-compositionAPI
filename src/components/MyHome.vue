<template>
  <div>{{ obj }}</div>
</template>

<script> 
import { reactive } from "vue"; // when using normal variables use ref

export default {
  setup() { 
    const obj = reactive({ counter: 0});
    setInterval(() => obj.counter++, 1000);

    return {
     obj,
    };
  },
};
</script>