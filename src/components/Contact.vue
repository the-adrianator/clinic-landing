<template>
  <section
    id="contact"
    class="py-20 overflow-hidden bg-linear-to-r from-pink-100 to-purple-100"
  >
    <div class="container mx-auto px-4">
      <!-- Header -->
      <header
        class="text-center mb-16 relative"
        data-aos="fade-up"
        data-aos-delay="400"
      >
        <span
          class="absolute -top-10 left-1/2 transform -translate-x-1/2 w-20 h-20 rounded-full bg-pink-100 opacity-30 z-0"
          aria-hidden="true"
        ></span>
        <h2
          id="contact-heading"
          class="text-3xl md:text-4xl font-bold text-gray-800 mb-4 relative"
        >
          Contact
          <span class="text-pink-600">Our Clinic</span>
        </h2>
        <p class="text-lg text-gray-600 max-w-2xl mx-auto relative z-10">
          Reach out to schedule your consultation or ask questions about our
          services
        </p>
        <span
          class="absolute -bottom-6 right-1/4 w-16 h-16 rounded-full bg-purple-100 opacity-20 z-0"
          aria-hidden="true"
        ></span>
      </header>

      <!-- Main Content -->
      <main class="flex flex-col lg:flex-row gap-12">
        <aside class="lg:w-2/5">
          <section
            data-aos="fade-up"
            data-aos-delay="500"
            class="bg-white rounded-2xl shadow-xl p-8 h-full"
          >
            <h2 class="text-2xl font-bold text-gray-800 mb-6">Get in Touch</h2>
            <address class="space-y-6">
              <article
                v-for="(item, index) in contactItems"
                :key="index"
                class="flex items-start"
              >
                <figure class="bg-pink-100 p-3 rounded-full mr-4 shrink-0">
                  <Icon :icon="item.icon" class="text-pink-600 text-xl" />
                </figure>
                <div>
                  <h3 class="font-semibold text-gray-800 mb-1">
                    {{ item.title }}
                  </h3>
                  <div v-html="item.content" class="text-gray-600"></div>
                </div>
              </article>
            </address>
            <figure class="mt-8 rounded-xl overflow-hidden shadow-md">
              <img
                src="@assets/contactImg.png"
                alt="Glades Clinic Building"
                width="400"
                height="200"
                loading="lazy"
                class="w-full h-48 object-cover hover:scale-105 transition-transform duration-500"
              />
            </figure>
          </section>
        </aside>

        <!-- Contact Form -->
        <section class="lg:w-3/5">
          <div
            data-aos="fade-up"
            data-aos-delay="600"
            class="bg-white rounded-2xl shadow-xl p-8 h-full"
          >
            <h2 class="text-2xl font-bold text-gray-800 mb-6">
              Send Us a Message
            </h2>
            <form class="space-y-6" @submit.prevent>
              <fieldset class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div>
                  <label for="name" class="block text-gray-700 font-medium mb-2"
                    >Full Name</label
                  >
                  <input
                    type="text"
                    id="name"
                    name="name"
                    placeholder="Your Full Name"
                    required="required"
                    class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-pink-500 focus:border--transparent"
                  />
                </div>
                <div>
                  <label
                    for="phone"
                    class="block text-gray-700 font-medium mb-2"
                    >Phone Number</label
                  >
                  <input
                    type="tel"
                    id="phone"
                    name="phone"
                    placeholder="+123-456-7890"
                    required="required"
                    class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-pink-500 focus:border--transparent"
                  />
                </div>
              </fieldset>
              <div>
                <label for="email" class="block text-gray-700 font-medium mb-2"
                  >Email Address</label
                >
                <input
                  type="email"
                  id="email"
                  name="email"
                  placeholder="your@email.com"
                  required="required"
                  class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-pink-500 focus:border--transparent"
                />
              </div>
              <div>
                <label
                  for="service"
                  class="block text-gray-700 font-medium mb-2"
                  >Service Requested</label
                >
                <select
                  id="service"
                  name="service"
                  required="required"
                  class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-pink-500 focus:border--transparent"
                >
                  <option value="">Select a Service</option>
                  <option
                    v-for="service in services"
                    :key="service.value"
                    :value="service.value"
                  >
                    {{ service.label }}
                  </option>
                </select>
              </div>
              <div>
                <label
                  for="message"
                  class="block text-gray-700 font-medium mb-2"
                  >Your Message</label
                >
                <textarea
                  id="message"
                  name="message"
                  placeholder="Tell us about your concerns or questions"
                  rows="5"
                  required="required"
                  class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-pink-500 focus:border--transparent"
                ></textarea>
              </div>
              <div>
                <button
                  type="submit"
                  aria-label="Submit Form"
                  class="bg-pink-600 hover:bg-pink-700 text-white px-8 py-3 rounded-full transition shadow-lg w-full md:w-auto cursor-pointer"
                >
                  Send Message
                </button>
              </div>
            </form>
          </div>
        </section>
      </main>

      <!-- Google Map -->
      <figure class="mt-16 bg-white rounded-2xl shadow-2xl overflow-hidden">
        <iframe
          src="https://www.openstreetmap.org/export/embed.html?bbox=-80.20507812500001%2C25.765625%2C-80.18798828125001%2C25.77606201171875&amp;layer=mapnik&amp;marker=25.770843505859375%2C-80.196533203125"
          frameborder="0"
          width="100%"
          height="450"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
          title="Clinic Location Map"
          aria-label="Clinic Location Map"
          class="rounded-2xl"
        ></iframe>
      </figure>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

const contactItems = ref([
  {
    icon: "fa-solid:map-marker-alt",
    title: "Our Location",
    content: `
		<p>123 Main St, Any City<br />Any State 112233, USA</p>
		`,
  },
  {
    icon: "fa-solid:phone-alt",
    title: "Phone Numbers",
    content: `
		<p>Appointments: <a href="tel:+1234567890" class='hover:text-pink-600'>+123-456-7890</a>
		<br />
		Emergencies: <a href="tel:+1238947948" class='hover:text-pink-600'>+123-894-7948</a>
		<br />
		General Inquiries: <a href="tel:+1230585936" class='hover:text-pink-600'>+123-058-5936</a>
		</p>
		`,
  },
  {
    icon: "fa-solid:envelope",
    title: "Email Us",
    content: `
		<p>General Inquiries: <a href="mailto:info@gladesclinic.com" class='hover:text-pink-600'>info@gladesclinic.com</a>
		<br />
		Appointment Requests: <a href="mailto:appointments@gladesclinic.com" class='hover:text-pink-600'>appointments@gladesclinic.com</a>
		<br />
		Technical Support: <a href="mailto:support@gladesclinic.com" class='hover:text-pink-600'>support@gladesclinic.com</a>
		</p>
		`,
  },
  {
    icon: "fa-solid:clock",
    title: "Office Hours",
    content: `
		<p>Monday - Friday: 9:00 AM - 5:00 PM</p>
		<p>Saturday: 10:00 AM - 2:00 PM</p>
		<p>Sunday: Closed</p>
		`,
  },
]);
const services = ref([
  { value: "botox", label: "Botox Treatments" },
  { value: "fillers", label: "Dermal Fillers" },
  { value: "laser", label: "Laser Therapy" },
  { value: "facelift", label: "Non-Surgical Facelift" },
  { value: "cool", label: "Cool Sculpting" },
  { value: "other", label: "Other Services" },
]);
</script>
