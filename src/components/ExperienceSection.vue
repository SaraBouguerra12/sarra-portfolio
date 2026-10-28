<script setup lang="ts">
const experiences = [
  {
    period: '06/07/2026 — 21/08/2026',
    role: 'AI & Full-Stack Development Intern',
    company: 'Smart IT Partner',
    location: 'Tunis, Tunisia',
    description:
      'Worked on EduAI, an AI-powered e-learning platform, contributing across the complete application lifecycle from development to automated deployment.',
    points: [
      'Developed AI services for content recommendation and automatic quiz generation using Python and FastAPI.',
      'Built backend services with Spring Boot and Angular interfaces for different platform roles.',
      'Worked with PostgreSQL, Docker and CI/CD using Jenkins.',
      'Implemented code quality analysis with SonarQube and monitoring with Prometheus and Grafana.'
    ],
    technologies: [
      'FastAPI',
      'Spring Boot',
      'Angular',
      'PostgreSQL',
      'Docker',
      'Jenkins'
    ]
  },
  {
    period: '07/2025 — 08/2025',
    role: 'Worker Intern',
    company: 'Tunisie Télécom',
    location: 'Tunis, Tunisia',
    description:
      'Discovered the technical environment of the telecommunications sector and gained initial professional experience working within an active team.',
    points: [],
    technologies: []
  },
  {
    period: '07/2023 — 08/2023',
    role: 'Web Development Intern',
    company: 'IT Innovation',
    location: 'Ariana, Tunisia',
    description:
      'Contributed to an online learning platform by implementing CRUD functionalities and interactive question-and-answer workflows.',
    points: [],
    technologies: ['JavaScript', 'Web Development']
  }
]
</script>

<template>
  <section id="experience" class="py-20 bg-gray-50 dark:bg-gray-900">
    <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">

      <div class="text-center mb-12">
        <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white">
          Experience
        </h2>
        <div class="w-20 h-1 bg-primary-600 mx-auto mt-4"></div>
      </div>

      <div class="space-y-8">
        <article
          v-for="experience in experiences"
          :key="experience.company + experience.period"
          class="bg-white dark:bg-gray-800 rounded-xl p-8 shadow-sm"
        >
          <div class="flex flex-col md:flex-row md:justify-between md:items-start mb-4">
            <div>
              <h3 class="text-2xl font-bold text-gray-900 dark:text-white">
                {{ experience.role }}
              </h3>

              <p class="text-primary-600 font-semibold mt-1">
                {{ experience.company }}
              </p>

              <p class="text-sm text-gray-500 dark:text-gray-400">
                {{ experience.location }}
              </p>
            </div>

            <span class="text-sm text-gray-500 dark:text-gray-400 mt-2 md:mt-0">
              {{ experience.period }}
            </span>
          </div>

          <p class="text-gray-600 dark:text-gray-300 leading-relaxed mb-4">
            {{ experience.description }}
          </p>

          <ul v-if="experience.points.length" class="space-y-2 mb-5">
            <li
              v-for="point in experience.points"
              :key="point"
              class="text-gray-600 dark:text-gray-300"
            >
              • {{ point }}
            </li>
          </ul>

          <div class="flex flex-wrap gap-2">
            <span
              v-for="tech in experience.technologies"
              :key="tech"
              class="px-3 py-1 bg-primary-50 dark:bg-gray-700 text-primary-700 dark:text-gray-200 rounded-full text-sm"
            >
              {{ tech }}
            </span>
          </div>
        </article>
      </div>

    </div>
  </section>
</template>