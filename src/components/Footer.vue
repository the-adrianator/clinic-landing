<template>
  <footer class="bg-gray-900 text-white pt-16 pb-8">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-12">
        <!-- Clinic info -->
        <section class="lg:col-span-2">
          <header class="flex items-center mb-6">
            <Icon
              icon="fa-solid:clinic-medical"
              aria-hidden="true"
              class="text-3xl text-pink-500 mr-3"
            />
            <h2 class="text-2xl font-bold">Glades Clinic</h2>
          </header>
          <p class="text-gray-400 mb-6">
            Premier cosmetic clinic dedicated to enhancing your natural beauty
            with state-of-the-art treatments and personalized expert care.
          </p>
          <nav aria-label="Social Media Links">
            <ul class="flex space-x-4">
              <li v-for="(link, index) in socialLinks" :key="index">
                <a
                  href="#"
                  target="_blank"
                  rel="noopener noreferrer"
                  :aria-label="link.label"
                  class="bg-gray-800 hover:bg-pink-600 w-10 h-10 rounded-full flex items-center justify-center transition-colors duration-200"
                >
                  <Icon :icon="link.icon" class="text-lg" aria-hidden="true" />
                </a>
              </li>
            </ul>
          </nav>
        </section>

        <!-- Quick Links -->
        <section>
          <h3
            class="text-xl font-bold mb-6 relative pb-2 after:content-[''] after:absolute after:bottom-0 after:left-0 after:w-12 after:h-1 after:bg-pink-500"
          >
            Quick Links
          </h3>
          <nav aria-label="Quick Links">
            <ul class="space-y-3">
              <li v-for="(link, index) in quickLinks" :key="index">
                <a
                  :href="link.href"
                  :aria-label="link.label"
                  class="text-gray-400 hover:text-pink-500 transition-colors duration-200"
                >
                  {{ link.label }}
                </a>
              </li>
            </ul>
          </nav>
        </section>

        <!-- Contact info -->
        <address>
          <h3
            class="text-xl font-bold mb-6 relative pb-2 after:content-[''] after:absolute after:bottom-0 after:left-0 after:w-12 after:h-1 after:bg-pink-500"
          >
            Contact Us
          </h3>
          <ul class="space-y-3">
            <li
              v-for="(contact, index) in contactInfo"
              :key="index"
              class="flex items-start"
            >
              <Icon
                :icon="contact.icon"
                class="text-pink-500 text-xl mt-1 mr-4 shrink-0"
              />
              <component
                :is="contact.content.type"
                v-bind="contact.content.props"
                class="text-gray-400 hover:text-pink-500 transition-colors duration-200"
                >{{ contact.content.text }}</component
              >
            </li>
          </ul>
        </address>
      </div>
      <!-- Newsletter -->
      <section
        class="bg-gray-800 rounded-xl px-8 py-6 mb-12"
        aria-labelledBy="newsletter-heading"
      >
        <div class="flex flex-col lg:flex-row items-center justify-between">
          <div class="mb-6 lg:mb-0 lg:mr-8">
            <h3 id="newsletter-heading" class="text-xl font-bold mb-2">
              Subscribe to our newsletter
            </h3>
            <p class="text-gray-400">
              Get updates on special offers and beauty tips
            </p>
          </div>
          <form
            action=""
            class="flex flex-col sm:flex-row w-full lg:w-auto"
            aria-label="Newsletter Subscription Form"
          >
            <label for="newsletter-email" class="sr-only"
              >Your email address</label
            ><input
              type="email"
              placeholder="Your email address"
              required="required"
              id="newsletter-email"
              class="px-6 py-3 rounded-full bg-gray-700 text-white focus:outline-none focus:ring-2 focus:ring-pink-500 mb-3 sm:mb-0 sm:mr-4 w-full"
            />
            <button
              type="submit"
              aria-label="Submit Form"
              class="bg-pink-600 hover:bg-pink-700 text-white px-8 py-3 rounded-full transition shadow-lg whitespace-nowrap cursor-pointer"
            >
              Subscribe
            </button>
          </form>
        </div>
      </section>
      <footer
        class="pt-8 border-t border-gray-800 flex flex-col md:flex-row justify-between items-center"
      >
        <p class="text-gray-500 text-sm mb-4 md:mb-0">
          &copy; {{ currentYear }} Glades Clinic. All rights reserved.
        </p>
        <nav aria-label="Legal Links">
          <ul class="flex space-x-6">
            <li v-for="(link, index) in legalLinks" :key="index">
              <a
                :href="link.href"
                :aria-label="link.label"
                class="text-gray-500 hover:text-pink-500 text-sm transition-colors duration-200"
              >
                {{ link.label }}
              </a>
            </li>
          </ul>
        </nav>
      </footer>
    </div>
  </footer>
</template>

<script setup>
import { ref, computed } from "vue";

const currentYear = computed(() => new Date().getFullYear());

const socialLinks = ref([
  {
    icon: "fa-brands:facebook-f",
    label: "Facebook",
  },
  {
    icon: "fa-brands:instagram",
    label: "Instagram",
  },
  {
    icon: "fa-brands:twitter",
    label: "Twitter",
  },
  {
    icon: "fa-brands:linkedin-in",
    label: "LinkedIn",
  },
  {
    icon: "fa-brands:youtube",
    label: "YouTube",
  },
]);

const quickLinks = ref([
  {
    href: "#",
    label: "Home",
  },
  {
    href: "#about",
    label: "About",
  },
  {
    href: "#services",
    label: "Our Services",
  },
  {
    href: "#specialists",
    label: "Our Specialists",
  },
  {
    href: "#contact",
    label: "Contact Us",
  },
  {
    href: "#appointment",
    label: "Book Appointment",
  },
]);

const contactInfo = ref([
  {
    icon: "material-symbols:location-on",
    content: {
      type: "a",
      props: {
        href: "#",
        target: "_blank",
        rel: "noopener noreferrer",
      },
      text: "123 Main St, Anytown, USA",
    },
  },
  {
    icon: "fa-solid:phone-alt",
    content: {
      type: "a",
      props: {
        href: "#",
      },
      text: "+123-456-7890",
    },
  },
  {
    icon: "material-symbols:mail",
    content: {
      type: "a",
      props: {
        href: "mailto:info@gladesclinic.com",
      },
      text: "info@gladesclinic.com",
    },
  },
  {
    icon: "fa-solid:clock",
    content: {
      type: "span",
      props: {},
      text: "Mon - Fri: 9:00 AM - 5:00 PM, Sat: 10:00 AM - 2:00 PM, Sun: Closed",
    },
  },
]);

const legalLinks = ref([
  {
    href: "#",
    label: "Privacy Policy",
  },
  {
    href: "#",
    label: "Terms of Service",
  },
  {
    href: "#",
    label: "Cookie Policy",
  },
  {
    href: "#",
    label: "Sitemap",
  },
]);
</script>
