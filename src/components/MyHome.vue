<template>
  <div>{{ fullName }}</div>
</template>

<script> 
import { computed, toRefs } from "vue";

export default {
  props: {
    firstName: String,
    lastName: String,
  },
  setup(props, { expose }) {
    console.log();
    const {firstName, lastName} = toRefs(props);

    const fullName = computed(() => {
      return `${firstName.value} ${lastName.value}`;
    }); 
    
    const foo = () => console.log();

    expose({
      fullName,
    });

    return {
      fullName,
      foo
    }
  },
};
</script>