<script>
import TheWelcome from '../components/TheWelcome.vue'
import {onMounted , ref} from "vue";

export default {
  components : { TheWelcome },

  setup() {

    onMounted(()=> {
      alert("Hi there!");
    });

    let message = ref("Hello world");

    setTimeout(()=>{
      message.value = "I have been changed!"; //Value of a string is accessed through .value in vue
    }, 3000);

    return {
      message,
    };
  },
}


</script>



<template>
  <main>
    <TheWelcome />
    <p>{{ message }}</p>
    <input type="text" v-model="message">
  </main>
</template>
