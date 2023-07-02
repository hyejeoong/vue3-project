<template>
  <div class="name"> 
    {{ name }} 
  </div>
  <input :type="type" :value="name">
  <button
      class = "btn btn-primary" 
      @click = "updatename" 
    >
    Click 
  
  </button>
  
</template>

<script>
import {ref} from 'vue';
export default {
 
  setup() {
    const name = ref('hyejeong');
    const type = ref('text');
    const nameclass = ref('name') 

    const updatename = () => {
     // console.log('hello world');
      name.value = 'shin';
      type.value = ('text');
    };
    // ref 템플릿 안에서는 value 없이 사용가능
    // const greet = greeting(name);

    return {
      name,
      updatename,
      type,
      nameclass,
    };

  }

}
</script>

<style>
  .name {  
    color: red;
  }

</style>