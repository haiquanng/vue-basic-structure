<template>
  <section class="py-20 bg-white">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
          What Our <span class="text-primary-600">Patients Say</span>
        </h2>
        <p class="text-xl text-gray-600 max-w-2xl mx-auto">
          Real stories from real people who have transformed their health journey with HealthVue.
        </p>
      </div>

      <!-- Testimonials Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="testimonial in testimonials"
          :key="testimonial.id"
          class="bg-gray-50 rounded-xl p-8 hover:shadow-lg transition-shadow duration-300"
        >
          <!-- Quote Icon -->
          <div class="text-primary-500 mb-4">
            <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 20 20">
              <path
                fill-rule="evenodd"
                d="M3 4a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm0 4a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm0 4a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm0 4a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
                clip-rule="evenodd"
              />
            </svg>
          </div>

          <!-- Testimonial Content -->
          <blockquote class="text-gray-700 mb-6 italic">"{{ testimonial.content }}"</blockquote>

          <!-- Rating -->
          <div class="flex items-center mb-4">
            <div class="flex space-x-1 mr-2">
              <svg
                v-for="star in 5"
                :key="star"
                class="w-4 h-4 text-yellow-400 fill-current"
                viewBox="0 0 20 20"
              >
                <path
                  d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"
                />
              </svg>
            </div>
            <span class="text-sm text-gray-600">{{ testimonial.rating }}/5</span>
          </div>

          <!-- Author Info -->
          <div class="flex items-center">
            <div
              class="w-12 h-12 bg-primary-500 rounded-full flex items-center justify-center text-white font-semibold mr-4"
            >
              {{ testimonial.initials }}
            </div>
            <div>
              <div class="font-semibold text-gray-900">{{ testimonial.name }}</div>
              <div class="text-sm text-gray-600">{{ testimonial.role }}</div>
            </div>
          </div>
        </div>
      </div>

      <!-- Stats Section -->
      <div class="mt-16 bg-primary-600 rounded-2xl p-8 md:p-12">
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8 text-center text-white">
          <div>
            <div class="text-3xl md:text-4xl font-bold mb-2">50K+</div>
            <div class="text-primary-200">Happy Patients</div>
          </div>
          <div>
            <div class="text-3xl md:text-4xl font-bold mb-2">200+</div>
            <div class="text-primary-200">Expert Doctors</div>
          </div>
          <div>
            <div class="text-3xl md:text-4xl font-bold mb-2">95%</div>
            <div class="text-primary-200">Success Rate</div>
          </div>
          <div>
            <div class="text-3xl md:text-4xl font-bold mb-2">4.9</div>
            <div class="text-primary-200">Average Rating</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const testimonials = ref([
  {
    id: 1,
    content:
      'HealthVue transformed my approach to wellness. The personalized recommendations and expert consultations helped me achieve my health goals faster than I ever imagined.',
    name: 'Sarah Johnson',
    role: 'Fitness Enthusiast',
    initials: 'SJ',
    rating: 5,
  },
  {
    id: 2,
    content:
      'The medication management feature is a game-changer. I never miss a dose anymore, and my health tracking gives me confidence in my progress.',
    name: 'Michael Chen',
    role: 'Chronic Patient',
    initials: 'MC',
    rating: 5,
  },
  {
    id: 3,
    content:
      'As a busy professional, having 24/7 access to healthcare guidance through HealthVue has been invaluable. The AI insights are remarkably accurate.',
    name: 'Emily Rodriguez',
    role: 'Business Executive',
    initials: 'ER',
    rating: 5,
  },
  {
    id: 4,
    content:
      'The secure health records feature gives me peace of mind. All my medical history is organized and accessible whenever I need it.',
    name: 'David Thompson',
    role: 'Retiree',
    initials: 'DT',
    rating: 5,
  },
  {
    id: 5,
    content:
      "HealthVue's expert consultations helped me understand my health better. The doctors are knowledgeable and truly care about patient outcomes.",
    name: 'Lisa Park',
    role: 'Teacher',
    initials: 'LP',
    rating: 5,
  },
  {
    id: 6,
    content:
      'The health tracking features motivated me to maintain better habits. Seeing my progress visualized keeps me committed to my wellness journey.',
    name: 'James Wilson',
    role: 'Software Developer',
    initials: 'JW',
    rating: 5,
  },
])
</script>
