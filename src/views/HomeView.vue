<script>
import TheWelcome from '../components/TheWelcome.vue'
import {onMounted} from "vue";

export default {
  components : { TheWelcome },

  setup() {

    onMounted(()=> {
      alert("Hi there!");
    })

    return {
      message : "Hello world",
    };
  },
}


</script>



<template>
  <main>
    <TheWelcome />
    <p>{{ message }}</p>
  </main>
</template>
