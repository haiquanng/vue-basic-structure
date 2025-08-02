<template>
  <section class="py-20 bg-gray-50">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
          Everything You Need for
          <span class="text-primary-600">Better Health</span>
        </h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto">
          Our comprehensive platform provides personalized health solutions backed by cutting-edge
          technology and expert care.
        </p>
      </div>

      <!-- Features Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="feature in features"
          :key="feature.id"
          class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2"
        >
          <div class="flex items-center justify-center w-16 h-16 bg-primary-100 rounded-full mb-6">
            <component :is="feature.icon" class="w-8 h-8 text-primary-600" />
          </div>
          <h3 class="text-xl font-semibold text-gray-900 mb-4">{{ feature.title }}</h3>
          <p class="text-gray-600 mb-6">{{ feature.description }}</p>
          <a
            href="#"
            class="inline-flex items-center text-primary-600 hover:text-primary-700 font-medium"
          >
            Learn more
            <svg class="w-4 h-4 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5l7 7-7 7"
              />
            </svg>
          </a>
        </div>
      </div>

      <!-- CTA Section -->
      <div class="mt-16 text-center">
        <div class="bg-white rounded-2xl p-8 md:p-12 shadow-xl">
          <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-4">
            Ready to Start Your Health Journey?
          </h3>
          <p class="text-gray-600 mb-8 max-w-2xl mx-auto">
            Join thousands of satisfied users who have transformed their health with our platform.
            Get started today with a free consultation.
          </p>
          <div class="flex flex-col sm:flex-row gap-4 justify-center">
            <button
              class="bg-primary-600 hover:bg-primary-700 text-white px-8 py-4 rounded-lg font-semibold transition-colors"
            >
              Book Free Consultation
            </button>
            <button
              class="border-2 border-primary-600 text-primary-600 hover:bg-primary-600 hover:text-white px-8 py-4 rounded-lg font-semibold transition-colors"
            >
              View Pricing
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue'

// Define feature data
const features = ref([
  {
    id: 1,
    title: 'Personal Health Tracking',
    description:
      'Monitor your vital signs, fitness goals, and health metrics with our advanced tracking system.',
    icon: 'ActivityIcon',
  },
  {
    id: 2,
    title: 'Expert Consultations',
    description:
      'Connect with certified healthcare professionals for personalized advice and treatment plans.',
    icon: 'UserGroupIcon',
  },
  {
    id: 3,
    title: 'AI Health Insights',
    description:
      'Get personalized recommendations and insights powered by advanced artificial intelligence.',
    icon: 'ChartBarIcon',
  },
  {
    id: 4,
    title: 'Medication Management',
    description: 'Never miss a dose with smart reminders and comprehensive medication tracking.',
    icon: 'ClockIcon',
  },
  {
    id: 5,
    title: 'Secure Health Records',
    description: 'Access your complete medical history securely from anywhere, anytime.',
    icon: 'ShieldCheckIcon',
  },
  {
    id: 6,
    title: '24/7 Support',
    description: 'Round-the-clock support from our dedicated healthcare assistance team.',
    icon: 'SupportIcon',
  },
])
</script>

<script lang="ts">
// Simple icon components
export default {
  components: {
    ActivityIcon: {
      template: `
        <svg fill="currentColor" viewBox="0 0 20 20">
          <path fill-rule="evenodd" d="M3 3a1 1 0 000 2v8a2 2 0 002 2h2.586l-1.293 1.293a1 1 0 101.414 1.414L10 15.414l2.293 2.293a1 1 0 001.414-1.414L12.414 15H15a2 2 0 002-2V5a1 1 0 100-2H3zm11.707 4.707a1 1 0 00-1.414-1.414L10 9.586 8.707 8.293a1 1 0 00-1.414 0l-2 2a1 1 0 001.414 1.414L8 10.414l1.293 1.293a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
        </svg>
      `,
    },
    UserGroupIcon: {
      template: `
        <svg fill="currentColor" viewBox="0 0 20 20">
          <path d="M13 6a3 3 0 11-6 0 3 3 0 016 0zM18 8a2 2 0 11-4 0 2 2 0 014 0zM14 15a4 4 0 00-8 0v3h8v-3zM6 8a2 2 0 11-4 0 2 2 0 014 0zM16 18v-3a5.972 5.972 0 00-.75-2.906A3.005 3.005 0 0119 15v3h-3zM4.75 12.094A5.973 5.973 0 004 15v3H1v-3a3 3 0 013.75-2.906z" />
        </svg>
      `,
    },
    ChartBarIcon: {
      template: `
        <svg fill="currentColor" viewBox="0 0 20 20">
          <path d="M2 11a1 1 0 011-1h2a1 1 0 011 1v5a1 1 0 01-1 1H3a1 1 0 01-1-1v-5zM8 7a1 1 0 011-1h2a1 1 0 011 1v9a1 1 0 01-1 1H9a1 1 0 01-1-1V7zM14 4a1 1 0 011-1h2a1 1 0 011 1v12a1 1 0 01-1 1h-2a1 1 0 01-1-1V4z" />
        </svg>
      `,
    },
    ClockIcon: {
      template: `
        <svg fill="currentColor" viewBox="0 0 20 20">
          <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z" clip-rule="evenodd" />
        </svg>
      `,
    },
    ShieldCheckIcon: {
      template: `
        <svg fill="currentColor" viewBox="0 0 20 20">
          <path fill-rule="evenodd" d="M2.166 4.999A11.954 11.954 0 0010 1.944 11.954 11.954 0 0017.834 5c.11.65.166 1.32.166 2.001 0 5.225-3.34 9.67-8 11.317C5.34 16.67 2 12.225 2 7c0-.682.057-1.35.166-2.001zm11.541 3.708a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
        </svg>
      `,
    },
    SupportIcon: {
      template: `
        <svg fill="currentColor" viewBox="0 0 20 20">
          <path fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-2 0c0 .993-.241 1.929-.668 2.754l-1.524-1.525a3.997 3.997 0 00.078-2.183l1.562-1.562C15.802 8.249 16 9.1 16 10zm-5.165 3.913l1.58 1.58A5.98 5.98 0 0110 16a5.976 5.976 0 01-2.516-.552l1.562-1.562a4.006 4.006 0 001.789.027zm-4.677-2.796a4.002 4.002 0 01-.041-2.08l-1.106-1.106A6.002 6.002 0 004 10c0 .639.1 1.255.283 1.832l1.555-1.555zm3.493-1.037L6.417 5.844c.62-.494 1.348-.844 2.139-.982L10 6.306l1.444-1.444c.791.138 1.518.488 2.139.982L12.349 9.08a4.034 4.034 0 00-4.698 0z" clip-rule="evenodd" />
        </svg>
      `,
    },
  },
}
</script>
