<script setup lang="ts">
const projects = [
  
{
  year: '2026',
  title: 'DataOps Lab — Reliable Data Pipeline',
  description:
    'A data engineering project that transforms daily sales orders into reliable revenue reports. It combines data validation, cleaning, SQL transformations with dbt and DuckDB, automated tests, CI and data versioning with DVC.',
  highlights: [
    'Data quality checks and rejected-row quarantine',
    'Revenue reporting by country',
    'dbt and DuckDB transformations',
    'DVC data versioning and reproducible pipelines',
    'Automated pytest tests and GitHub Actions CI'
  ],
  technologies: [
    'Python',
    'Pandas',
    'SQL',
    'dbt',
    'DuckDB',
    'DVC',
    'pytest',
    'GitHub Actions'
  ],
  github: 'https://github.com/SaraBouguerra12/dataops-lab1',
  note: ''
},

  {
    year: '2026',
    title: 'EduAI — AI-powered E-Learning Platform',
    description:
      'Complete e-learning platform developed during my internship at Smart IT Partner. The platform combines learning management, analytics and AI-powered services such as quiz generation and content recommendation.',
    highlights: [
      'AI-powered quiz generation',
      'Content recommendation',
      'Analytics dashboard',
      'Multi-role platform'
    ],
    technologies: [
      'FastAPI',
      'Spring Boot',
      'Angular',
      'PostgreSQL',
      'Docker',
      'Jenkins'
    ],
    github: null,
    note: 'Professional project — source code is private.'
  },

  {
    year: '2025',
    title: 'Vehicule Type Classification',
    description:
      'Machine learning classifier trained on 18 vehicle characteristics to distinguish between four vehicle types and exposed through a REST API with a web interface.',
    highlights: [
      '82.63% test accuracy',
      '84.83% cross-validation score',
      '18 features',
      'Random Forest classifier'
    ],
    technologies: [
      'Python',
      'Scikit-learn',
      'Pandas',
      'Flask'
    ],
    github: 'https://github.com/SaraBouguerra12/projet-vehicules',
    note: ''
  },

  {
    year: '2025',
    title: 'Data Governance Dashboard',
    description:
      'Data governance framework simulation built around synthetic pipeline logs, data quality scores and monitored tables, presented through an interactive Tableau dashboard.',
    highlights: [
      '6 dashboard views',
      '200 monitored tables',
      '5,200 quality scores',
      '10,000 pipeline logs'
    ],
    technologies: [
      'Python',
      'Pandas',
      'Tableau',
      'CRISP-DM'
    ],
    github: 'https://github.com/SaraBouguerra12/Gouvernance-Data',
    note: ''
  },

  {
    year: '2025',
    title: 'RechargeMe — EV Charging Platform',
    description:
      'Mobile application for locating and booking electric vehicle charging stations, with a Django REST API for authentication and station management.',
    highlights: [
      'EV station discovery',
      'Station booking',
      'REST API',
      'Mobile map interface'
    ],
    technologies: [
      'Flutter',
      'Django REST',
      'SQLite'
    ],
    github: 'https://github.com/SaraBouguerra12/RechargeMe',
    note: ''
  }
]
</script>

<template>
  <section id="projects" class="py-20 bg-white dark:bg-gray-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">

      <div class="text-center mb-12">
        <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white">
          Featured Projects
        </h2>

        <div class="w-20 h-1 bg-primary-600 mx-auto mt-4"></div>

        <p class="text-gray-600 dark:text-gray-300 mt-4 max-w-2xl mx-auto">
          From machine learning models to complete AI-powered applications.
        </p>
      </div>

      <div class="grid md:grid-cols-2 gap-8">

        <article
          v-for="project in projects"
          :key="project.title"
          class="bg-gray-50 dark:bg-gray-900 rounded-xl p-6 shadow-sm hover:shadow-lg transition-shadow"
        >

          <div class="flex justify-between items-start mb-4">
            <span class="text-primary-600 font-semibold">
              {{ project.year }}
            </span>
          </div>

          <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-3">
            {{ project.title }}
          </h3>

          <p class="text-gray-600 dark:text-gray-300 mb-5 leading-relaxed">
            {{ project.description }}
          </p>

          <div class="mb-5">
            <ul class="space-y-2">
              <li
                v-for="highlight in project.highlights"
                :key="highlight"
                class="text-sm text-gray-600 dark:text-gray-300"
              >
                ✓ {{ highlight }}
              </li>
            </ul>
          </div>

          <div class="flex flex-wrap gap-2 mb-6">
            <span
              v-for="tech in project.technologies"
              :key="tech"
              class="px-3 py-1 bg-primary-50 dark:bg-gray-700 text-primary-700 dark:text-gray-200 rounded-full text-sm"
            >
              {{ tech }}
            </span>
          </div>

          <div class="flex items-center gap-4">

            <a
              v-if="project.github"
              :href="project.github"
              target="_blank"
              rel="noopener noreferrer"
              class="text-primary-600 hover:text-primary-700 font-medium"
            >
              GitHub →
            </a>

            <span
              v-if="project.note"
              class="text-sm text-gray-500 dark:text-gray-400"
            >
              {{ project.note }}
            </span>

          </div>

        </article>

      </div>
    </div>
  </section>
</template>