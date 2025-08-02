<template>
  <header
    class="fixed top-0 left-0 right-0 z-50 bg-white/90 backdrop-blur-sm border-b border-gray-100"
  >
    <nav class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-16">
        <!-- Logo -->
        <div class="flex items-center">
          <router-link to="/" class="flex items-center space-x-2">
            <div
              class="w-8 h-8 bg-linear-to-r from-primary-500 to-primary-600 rounded-lg flex items-center justify-center"
            >
              <svg class="w-5 h-5 text-white" fill="currentColor" viewBox="0 0 20 20">
                <path
                  fill-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  clip-rule="evenodd"
                />
              </svg>
            </div>
            <span class="text-xl font-bold text-primary-700">HealthVue</span>
          </router-link>
        </div>

        <!-- Desktop Navigation -->
        <div class="hidden md:flex items-center space-x-8">
          <router-link
            to="/"
            class="text-gray-700 hover:text-primary-600 transition-colors font-medium"
            :class="{ 'text-primary-600': $route.path === '/' }"
          >
            Home
          </router-link>
          <router-link
            to="/services"
            class="text-gray-700 hover:text-primary-600 transition-colors font-medium"
            :class="{ 'text-primary-600': $route.path === '/services' }"
          >
            Services
          </router-link>
          <router-link
            to="/about"
            class="text-gray-700 hover:text-primary-600 transition-colors font-medium"
            :class="{ 'text-primary-600': $route.path === '/about' }"
          >
            About
          </router-link>
          <router-link
            to="/contact"
            class="text-gray-700 hover:text-primary-600 transition-colors font-medium"
            :class="{ 'text-primary-600': $route.path === '/contact' }"
          >
            Contact
          </router-link>
        </div>

        <!-- CTA Button -->
        <div class="hidden md:flex items-center space-x-4">
          <button
            class="bg-primary-600 hover:bg-primary-700 text-white px-6 py-2 rounded-lg font-medium transition-colors"
          >
            Book Consultation
          </button>
        </div>

        <!-- Mobile menu button -->
        <div class="md:hidden">
          <button
            @click="mobileMenuOpen = !mobileMenuOpen"
            class="text-gray-700 hover:text-primary-600 transition-colors"
          >
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              />
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Navigation -->
      <div v-if="mobileMenuOpen" class="md:hidden bg-white border-t border-gray-100">
        <div class="px-4 py-4 space-y-4">
          <router-link
            to="/"
            class="block text-gray-700 hover:text-primary-600 transition-colors font-medium"
            @click="mobileMenuOpen = false"
          >
            Home
          </router-link>
          <router-link
            to="/services"
            class="block text-gray-700 hover:text-primary-600 transition-colors font-medium"
            @click="mobileMenuOpen = false"
          >
            Services
          </router-link>
          <router-link
            to="/about"
            class="block text-gray-700 hover:text-primary-600 transition-colors font-medium"
            @click="mobileMenuOpen = false"
          >
            About
          </router-link>
          <router-link
            to="/contact"
            class="block text-gray-700 hover:text-primary-600 transition-colors font-medium"
            @click="mobileMenuOpen = false"
          >
            Contact
          </router-link>
          <button
            class="w-full bg-primary-600 hover:bg-primary-700 text-white px-6 py-2 rounded-lg font-medium transition-colors mt-4"
          >
            Book Consultation
          </button>
        </div>
      </div>
    </nav>
  </header>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const mobileMenuOpen = ref(false)
</script>
