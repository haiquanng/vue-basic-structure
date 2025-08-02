<template>
  <section
    class="relative min-h-screen flex items-center justify-center gradient-bg hero-pattern overflow-hidden"
  >
    <!-- Background Elements -->
    <div class="absolute inset-0">
      <div class="absolute top-10 left-10 w-20 h-20 bg-white/10 rounded-full animate-pulse"></div>
      <div
        class="absolute top-32 right-20 w-16 h-16 bg-white/10 rounded-full animate-pulse delay-1000"
      ></div>
      <div
        class="absolute bottom-20 left-1/4 w-12 h-12 bg-white/10 rounded-full animate-pulse delay-2000"
      ></div>
      <div
        class="absolute bottom-32 right-1/3 w-8 h-8 bg-white/10 rounded-full animate-pulse delay-3000"
      ></div>
    </div>

    <div class="container mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <!-- Text Content -->
        <div class="text-white">
          <div class="mb-6">
            <span
              class="inline-block bg-white/20 text-white px-4 py-2 rounded-full text-sm font-medium mb-4"
            >
              🌟 Your Health, Our Priority
            </span>
            <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
              Transform Your
              <span class="block text-primary-200">Health Journey</span>
              Today
            </h1>
            <p class="text-xl text-primary-100 mb-8 max-w-lg">
              Experience personalized healthcare that adapts to your lifestyle. Our comprehensive
              platform connects you with expert professionals and cutting-edge health solutions.
            </p>
          </div>

          <div class="flex flex-col sm:flex-row gap-4 mb-8">
            <button
              class="bg-white text-primary-600 hover:bg-primary-50 px-8 py-4 rounded-lg font-semibold transition-all duration-300 transform hover:scale-105 shadow-lg"
            >
              Start Your Journey
            </button>
            <button
              class="border-2 border-white text-white hover:bg-white hover:text-primary-600 px-8 py-4 rounded-lg font-semibold transition-all duration-300"
            >
              Watch Demo
            </button>
          </div>

          <!-- Stats -->
          <div class="grid grid-cols-3 gap-6">
            <div class="text-center">
              <div class="text-2xl font-bold text-white">50K+</div>
              <div class="text-primary-200 text-sm">Happy Patients</div>
            </div>
            <div class="text-center">
              <div class="text-2xl font-bold text-white">95%</div>
              <div class="text-primary-200 text-sm">Success Rate</div>
            </div>
            <div class="text-center">
              <div class="text-2xl font-bold text-white">24/7</div>
              <div class="text-primary-200 text-sm">Support</div>
            </div>
          </div>
        </div>

        <!-- Image/Illustration -->
        <div class="relative">
          <div class="relative z-10">
            <!-- Health Dashboard Mockup -->
            <div
              class="bg-white rounded-2xl shadow-2xl p-6 transform rotate-3 hover:rotate-0 transition-transform duration-500"
            >
              <div class="bg-primary-50 rounded-lg p-4 mb-4">
                <div class="flex items-center justify-between mb-3">
                  <h3 class="font-semibold text-gray-800">Health Dashboard</h3>
                  <div class="w-3 h-3 bg-primary-500 rounded-full animate-pulse"></div>
                </div>

                <!-- Progress Bars -->
                <div class="space-y-3">
                  <div>
                    <div class="flex justify-between text-sm text-gray-600 mb-1">
                      <span>Steps Today</span>
                      <span>8,547 / 10,000</span>
                    </div>
                    <div class="w-full bg-gray-200 rounded-full h-2">
                      <div class="bg-primary-500 h-2 rounded-full" style="width: 85%"></div>
                    </div>
                  </div>

                  <div>
                    <div class="flex justify-between text-sm text-gray-600 mb-1">
                      <span>Water Intake</span>
                      <span>6 / 8 glasses</span>
                    </div>
                    <div class="w-full bg-gray-200 rounded-full h-2">
                      <div class="bg-blue-500 h-2 rounded-full" style="width: 75%"></div>
                    </div>
                  </div>

                  <div>
                    <div class="flex justify-between text-sm text-gray-600 mb-1">
                      <span>Sleep Quality</span>
                      <span>7.5 hours</span>
                    </div>
                    <div class="w-full bg-gray-200 rounded-full h-2">
                      <div class="bg-purple-500 h-2 rounded-full" style="width: 90%"></div>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Health Metrics -->
              <div class="grid grid-cols-2 gap-4">
                <div class="bg-red-50 rounded-lg p-3 text-center">
                  <div class="text-2xl font-bold text-red-600">72</div>
                  <div class="text-xs text-red-600">Heart Rate</div>
                </div>
                <div class="bg-blue-50 rounded-lg p-3 text-center">
                  <div class="text-2xl font-bold text-blue-600">120/80</div>
                  <div class="text-xs text-blue-600">Blood Pressure</div>
                </div>
              </div>
            </div>
          </div>

          <!-- Floating Elements -->
          <div
            class="absolute -top-6 -right-6 w-12 h-12 bg-yellow-400 rounded-full flex items-center justify-center animate-bounce"
          >
            <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 20 20">
              <path
                fill-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                clip-rule="evenodd"
              />
            </svg>
          </div>

          <div
            class="absolute -bottom-4 -left-4 w-16 h-16 bg-pink-400 rounded-full flex items-center justify-center animate-pulse"
          >
            <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 20 20">
              <path
                d="M3.172 5.172a4 4 0 015.656 0L10 6.343l1.172-1.171a4 4 0 115.656 5.656L10 17.657l-6.828-6.829a4 4 0 010-5.656z"
              />
            </svg>
          </div>
        </div>
      </div>
    </div>

    <!-- Scroll Indicator -->
    <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
      <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M19 14l-7 7m0 0l-7-7m7 7V3"
        />
      </svg>
    </div>
  </section>
</template>

<script setup lang="ts">
// Component logic can be added here if needed
</script>
