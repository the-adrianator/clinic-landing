<template>
  <header class="bg-linear-to-r from-pink-100 to-purple-100 sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center">
      <!-- Logo -->
      <a
        href="/"
        class="flex items-center focus:outline-none focus:ring-2 focus:ring-pink-600 rounded"
      >
        <img
          src="@assets/logo.png"
          alt="Glades Clinic Logo"
          class="w-10 h-10"
        />
        Glades Clinic
      </a>

      <!-- Desktop navigation -->
      <nav class="hidden lg:flex space-x-6" aria-label="Primary navigation">
        <a
          v-for="(link, index) in navLinks"
          :key="index"
          :href="link.href"
          class="text-gray-700 hover:text-pink-600 px-4 transition-colors duration-200 focus:outline-none focus:ring-2 focus:ring-pink-600 rounded"
          >{{ link.label }}</a
        >
      </nav>

      <!-- Appointment Button (Desktop) -->
      <div class="hidden lg:block">
        <a
          href="#appointment"
          class="bg-linear-to-r from-pink-500 to-purple-500 text-white px-6 py-2 rounded-full hover:from-pink-600 hover:to-purple-600 transition-all duration-300 focus:outline-none focus:ring-2 focus:ring-pink-600 focus:ring-offset-2"
          >Book Appointment</a
        >
      </div>

      <!-- Mobile Menu Button -->
      <button
        type="button"
        class="lg:hidden focus:outline-none focus:ring-2 focus:ring-pink-600 rounded"
        aria-label="Toggle menu"
        @click="toggleMenu"
        :aria-expanded="isMobileMenuOpen.toString()"
        aria-controls="mobile-menu"
      >
        <Icon
          :icon="isMobileMenuOpen ? 'mdi:close' : 'mdi:menu'"
          class="w-6 h-6"
        />
      </button>
    </div>

    <!-- Mobile Menu -->
    <aside
      v-if="isMobileMenuOpen"
      id="mobile-menu"
      class="lg:hidden bg-white shadow-lg py-4 px-4 absolute top-full left-0 right-0 z-40"
      aria-label="Mobile menu"
    >
      <nav aria-label="Mobile navigation">
        <ul class="flex flex-col space-y-4">
          <li v-for="(link, index) in navLinks" :key="index">
            <a
              :href="link.href"
              class="block text-gray-700 hover:text-pink-600 transition-colors duration-200 py-2 px-2 focus:outline-none focus:ring-2 focus:ring-pink-600 rounded"
              @click="toggleMenu"
              >{{ link.label }}</a
            >
          </li>

          <li>
            <a
              href="#appointment"
              class="block bg-pink-600 hover:bg-pink-700 text-white px-4 py-2 rounded-full transition-colors duration-200 shadow-md focus:outline-none focus:ring-2 focus:ring-pink-800 focus:ring-offset-2"
              @click="toggleMenu"
            >
              Book Appointment
            </a>
          </li>
        </ul>
      </nav>
    </aside>
  </header>
</template>

<script setup>
import { ref } from "vue";

const navLinks = ref([
  { label: "Home", href: "#home" },
  { label: "Services", href: "#services" },
  { label: "About Us", href: "#about" },
  { label: "Our Specialists", href: "#specialists" },
  { label: "Contact Us", href: "#contact" },
]);

const isMobileMenuOpen = ref(false);

const toggleMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value;
};
</script>

<style scoped></style>
