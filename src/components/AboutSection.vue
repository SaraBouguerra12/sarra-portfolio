<script setup lang="ts">
const info = [
  ['Location', 'Tunis, Tunisia'],
  ['Looking for', 'Final-Year Internship · 4–6 months'],
  ['Availability', 'February 2027'],
  ['Languages', 'Arabic · French · English']
]
</script>

<template>
  <section id="about" class="py-20 bg-white dark:bg-gray-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">

      <div class="text-center mb-12">
        <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white">
          About Me
        </h2>
        <div class="w-20 h-1 bg-primary-600 mx-auto mt-4"></div>
      </div>

      <div class="max-w-4xl mx-auto">

        <p class="text-lg text-gray-600 dark:text-gray-300 leading-relaxed mb-6">
          I am a Data Science and AI Engineering student at Sesame University,
          with a strong interest in machine learning, deep learning, natural
          language processing and data engineering.
        </p>

        <p class="text-lg text-gray-600 dark:text-gray-300 leading-relaxed mb-6">
          Beyond building models, I enjoy understanding how an idea becomes
          a usable product — from data preparation and model development to
          API integration, application development and deployment.
        </p>

        <p class="text-lg text-gray-600 dark:text-gray-300 leading-relaxed mb-10">
          My recent experience on an AI-powered e-learning platform allowed me
          to work across the full lifecycle of a real application, combining
          AI services, backend development, databases, CI/CD and monitoring.
        </p>

        <div class="grid sm:grid-cols-2 gap-4">
          <div
            v-for="item in info"
            :key="item[0]"
            class="bg-gray-50 dark:bg-gray-900 rounded-lg p-4"
          >
            <p class="text-sm text-gray-500 dark:text-gray-400">
              {{ item[0] }}
            </p>

            <p class="font-semibold text-gray-900 dark:text-white mt-1">
              {{ item[1] }}
            </p>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>