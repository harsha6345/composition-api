<script setup>
import TheWelcome from '../components/TheWelcome.vue'
import { useFlash } from "@/composables/useFlash"

const { flash } = useFlash();
</script>

<template>
  <main>
    <TheWelcome />
    <p>{{ message }}</p>
    <button @click="flash('it works')">Flash</button>
  </main>
</template>
