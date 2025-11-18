<template>
	<section id="about" class="py-14 overflow-hidden bg-linear-to-br from-pink-100 to-purple-100">
		<div class="container mx-auto px-4" data-aos="fade-up" data-aos-delay="400">
			<article class="flex flex-col lg:flex-row items-center gap-12">
				<figure class="lg:w-5/12 relative">
					<div class="relative z-10 rounded-2xl overflow-hidden shadow-2xl w-full max-w-md mx-auto">
						<img src="@assets/aboutImage.png" alt="About Glades Clinic" class="w-full h-auto object-cover" loading="lazy">
						<div class="absolute inset-0 bg-linear-to-t from-black/40 to-transparent" aria-hidden="true" />
					</div>

					<!-- Decorative Elements -->
					<span class="hidden lg:block absolute -bottom-8 -left-8 w-32 h-32 rounded-full bg-pink-500 opacity-20 z-0" aria-hidden="true"></span><span class="hidden lg:block absolute -top-8 -right-8 w-32 h-32 rounded-full bg-pink-500 opacity-20 z-0" aria-hidden="true"></span>
				</figure>

				<!-- Content Column -->
				 <div class="lg:w-7/12" data-aos="fade-up" data-aos-delay="600">
					<header>
						<h2 id="about-heading" class="text-3xl md:text-4xl font-bold text-gray-800 mb-6">
							About
							<span class="text-pink-600">Glades Clinic</span>
						</h2>
						<p class="text-lg text-gray-600 mb-6">Glades Clinic is a leading provider of healthcare services in the United States. We are committed to providing the highest quality of care to our patients.</p>
					</header>

					<section class="mb-8">
						<h3 class="text-xl font-semibold text-gray-800 mb-4">Our Approach</h3>
						<ul class="space-y-3">
							<li v-for="(approach, index) in approaches" :key="index" class="flex items-start">
								<figure class="bg-pink-100 p-1 rounded-full mr-3">
									<Icon class="text-pink-600" :icon="approach.icon" aria-hidden="true" />
								</figure>
								<p class="text-gray-700">{{ approach.text }}</p>
							</li>
						</ul>
					</section>

					<!-- Stats Section -->
					 <section class="grid grid-cols-2 gap-4 mb-8">
						<article class="bg-white p-4 rounded-lg shadow-sm flex items-center" v-for="(stat, index) in stats" :key="index">
							<figure class="mr-3">
								<Icon :icon="stat.icon" aria-hidden="true" class="text-pink-500" />
							</figure>
							<div>
								<strong class="text-xl font-bold text-gray-800">{{ stat.value }}</strong>
								<p class="text-sm text-gray-600">{{ stat.label }}</p>
							</div>
						</article>
					 </section>
					 <nav><a href="#appointment" class="bg-pink-600 hover:bg-pink-700 text-white text-center px-6 py-3 rounded-full inline-block transition shadow-lg focus:outline-none focus:ring-2 focus:ring-pink-800 focus:ring-offset-2">Meet Our Specialists</a></nav>
				 </div>
			</article>

			<!-- Mission Statement -->
			 <aside class="mt-20 bg-white rounded-2xl p-8 md:p-12 shadow-lg relative overflow-hidden">
				<span class="absolute -top-20 -right-20 w-64 h-64 rounded-full bg-pink-500 opacity-40" aria-hidden="true"></span>
				<div class="relative z-10">
					<h3 class="text-2xl font-bold text-gray-800 mb-6">Our Mission</h3>
					<blockquote class="text-lg text-gray-700 mb-6">
						Our mission is to provide the highest quality of care to our patients. We are committed to providing the highest quality of care to our patients. 
					</blockquote>
					<figure class="flex items-center">
						<div class="w-12 h-12 rounded-full bg-pink-100 flex items-center justify-center mr-4">
							<Icon class="text-pink-600" icon="fa-solid:user-md" aria-hidden="true" />
							</div>
							<figcaption>
								<cite class="font-semibold text-gray-800 not-italic">Dr. Jean Glades</cite>
								<p class="text-sm text-gray-600">Medical Director & Founder</p>
							</figcaption>
					</figure>
				</div>
			 </aside>
		</div>
	</section>
</template>

<script setup>
import { ref } from 'vue'

const approaches = ref([
	{
		icon: 'fa-solid:heart',
		text: 'Personalized treatment plans tailored to your unique needs'
	},
	{
		icon: 'fa-solid:clinic-medical',
		text: 'Expert medical care from a team of experienced professionals'
	},
	{
		icon: 'fa-solid:calendar-check',
		text: 'Convenient scheduling and easy access to care'
	}
])

const stats = ref([
	{
		icon: 'fa-solid:award',
		value: '10+',
		label: 'Years Experience'
	},
	{
		icon: 'fa-solid:heart',
		value: '2.5k+',
		label: 'Happy Clients'
	},
	{
		icon: 'fa-solid:user-md',
		value: '15+',
		label: 'Medical Professionals'
	},
	{
		icon: 'fa-solid:clinic-medical',
		value: '50+',
		label: 'Treatments Offered'
	}
])
</script>

<style>

</style>