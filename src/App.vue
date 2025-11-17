<template>
  <div>
    <h1 class="text-3xl font-bold underline">Hello World</h1>
  </div>
</template>

<script setup>
import { onMounted } from 'vue'
import AOS from 'aos'
import 'aos/dist/aos.css'
onMounted(() => {
  AOS.init()
})
</script>