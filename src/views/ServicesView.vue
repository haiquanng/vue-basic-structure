<template>
  <div class="pt-16">
    <!-- Hero Section -->
    <section class="bg-primary-600 text-white py-20">
      <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center">
          <h1 class="text-4xl md:text-5xl font-bold mb-6">Our Health Services</h1>
          <p class="text-xl text-primary-100 max-w-3xl mx-auto">
            Comprehensive healthcare solutions designed to meet your unique needs and support your
            wellness journey.
          </p>
        </div>
      </div>
    </section>

    <!-- Services Grid -->
    <section class="py-20 bg-gray-50">
      <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div
            v-for="service in services"
            :key="service.id"
            class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300"
          >
            <div class="text-primary-600 mb-6">
              <component :is="service.icon" class="w-12 h-12" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-4">{{ service.title }}</h3>
            <p class="text-gray-600 mb-6">{{ service.description }}</p>
            <div class="text-2xl font-bold text-primary-600 mb-4">{{ service.price }}</div>
            <ul class="space-y-2 mb-6">
              <li
                v-for="feature in service.features"
                :key="feature"
                class="flex items-center text-gray-600"
              >
                <svg class="w-4 h-4 text-primary-500 mr-2" fill="currentColor" viewBox="0 0 20 20">
                  <path
                    fill-rule="evenodd"
                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                    clip-rule="evenodd"
                  />
                </svg>
                {{ feature }}
              </li>
            </ul>
            <button
              class="w-full bg-primary-600 hover:bg-primary-700 text-white py-3 rounded-lg font-semibold transition-colors"
            >
              Choose Plan
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="py-20 bg-white">
      <div class="container mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-6">Need a Custom Solution?</h2>
        <p class="text-xl text-gray-600 mb-8 max-w-2xl mx-auto">
          Our team can create a personalized health plan tailored specifically to your needs and
          goals.
        </p>
        <button
          class="bg-primary-600 hover:bg-primary-700 text-white px-8 py-4 rounded-lg font-semibold transition-colors"
        >
          Contact Our Specialists
        </button>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const services = ref([
  {
    id: 1,
    title: 'Basic Health Monitoring',
    description: 'Essential health tracking and basic consultations for everyday wellness.',
    price: '$29/month',
    icon: 'HeartIcon',
    features: [
      'Daily health tracking',
      'Basic health metrics',
      '1 consultation per month',
      'Email support',
      'Mobile app access',
    ],
  },
  {
    id: 2,
    title: 'Comprehensive Care',
    description: 'Advanced health management with personalized care plans and regular check-ins.',
    price: '$79/month',
    icon: 'UserIcon',
    features: [
      'Advanced health analytics',
      'Personalized care plans',
      '4 consultations per month',
      '24/7 chat support',
      'Medication management',
      'Health goal tracking',
    ],
  },
  {
    id: 3,
    title: 'Premium Wellness',
    description:
      'Complete health ecosystem with unlimited access to specialists and premium features.',
    price: '$149/month',
    icon: 'StarIcon',
    features: [
      'Unlimited consultations',
      'Specialist referrals',
      'AI health insights',
      'Priority support',
      'Family plan options',
      'Advanced health reports',
      'Wellness coaching',
    ],
  },
])
</script>

<script lang="ts">
export default {
  components: {
    HeartIcon: {
      template: `
        <svg fill="currentColor" viewBox="0 0 20 20">
          <path fill-rule="evenodd" d="M3.172 5.172a4 4 0 015.656 0L10 6.343l1.172-1.171a4 4 0 115.656 5.656L10 17.657l-6.828-6.829a4 4 0 010-5.656z" clip-rule="evenodd" />
        </svg>
      `,
    },
    UserIcon: {
      template: `
        <svg fill="currentColor" viewBox="0 0 20 20">
          <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd" />
        </svg>
      `,
    },
    StarIcon: {
      template: `
        <svg fill="currentColor" viewBox="0 0 20 20">
          <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
        </svg>
      `,
    },
  },
}
</script>
