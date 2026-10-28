<script setup lang="ts">
const technologies = [
  'Python',
  'SQL',
  'Machine Learning',
  'FastAPI',
  'Spring Boot',
  'PostgreSQL',
  'Docker',
  'MLflow',
  'Jenkins',
  'Git'
]
</script>

<template>
  <section
    class="min-h-screen flex items-center justify-center bg-gradient-to-br from-primary-50 to-white dark:from-gray-900 dark:to-gray-800"
  >
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-32">
      <div class="text-center">

        <p class="text-lg sm:text-xl font-medium text-primary-600 mb-4">
          Hi, I'm Sarra Bouguerra
        </p>

        <h1 class="text-4xl sm:text-6xl font-bold text-gray-900 dark:text-white mb-6">
          Data Science &
          <span class="text-primary-600">AI Engineer</span>
        </h1>

        <p class="text-xl text-gray-600 dark:text-gray-300 mb-8 max-w-3xl mx-auto">
          I build data-driven systems that go from raw data to production:
          machine learning models, AI services and complete applications,
          deployed with modern DevOps practices.
        </p>

        <p class="text-lg text-gray-500 dark:text-gray-400 mb-8">
          Available for a
          <span class="font-semibold text-primary-600">
            Final-Year Internship (PFE)
          </span>
          from February 2027.
        </p>

        <div class="flex flex-wrap justify-center gap-4 mb-12">

          <a
            href="#projects"
            class="bg-primary-600 text-white px-8 py-3 rounded-full hover:bg-primary-700 transition-colors"
          >
            View My Projects
          </a>

          <a
            href="#contact"
            class="border-2 border-primary-600 text-primary-600 px-8 py-3 rounded-full hover:bg-primary-50 transition-colors"
          >
            Get in Touch
          </a>

        </div>

        <div class="flex flex-wrap justify-center gap-4">
          <span
            v-for="tech in technologies"
            :key="tech"
            class="px-4 py-2 bg-white dark:bg-gray-800 rounded-full text-sm shadow-sm"
          >
            {{ tech }}
          </span>
        </div>

      </div>
    </div>
  </section>
</template>