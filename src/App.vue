<template>

  <input 
    type="type" 
    v-model="name"
  >
  <button
      class = "btn btn-primary" 
      @click = "onSubmit" 
    >
    Click 
  
  </button>
  
</template>

<script>
import {ref} from 'vue';
export default {
 
  setup() {
    const name = ref('hyejeong');

    const onSubmit = () => {
      alert(name.value);
    };
    // ref 템플릿 안에서는 value 없이 사용가능
    // const greet = greeting(name);

    return {
      name,
      onSubmit,
    };

  }

}
</script>

<style>
  .name {  
    color: red;
  }

</style>