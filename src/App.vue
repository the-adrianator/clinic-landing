<template>
  <div>
    <Header />
    <Hero />
    <Services />
    <About />
    <Specialists />
    <Contact />
  </div>
</template>

<script setup>
import { onMounted } from "vue";
import Header from "@components/Header.vue";
import Hero from "@components/Hero.vue";
import Services from "@components/Services.vue";
import About from "@components/About.vue";
import Specialists from "@components/Specialists.vue";
import Contact from "@components/Contact.vue";
import AOS from "aos";
import "aos/dist/aos.css";

onMounted(() => {
  AOS.init();
});
</script>
