<script setup lang="ts">
const skillCategories = [
  {
    title: 'Data Science',
    skills: [
      'Python',
      'Pandas',
      'NumPy',
      'Scikit-learn',
      'Machine Learning',
      'Deep Learning',
      'NLP',
      'SQL'
    ]
  },
  {
    title: 'AI & LLMs',
    skills: [
      'FastAPI',
      'OpenAI API',
      'LangChain',
      'Prompt Engineering',
      'Recommendation Systems',
      'AI Services'
    ]
  },
  {
    title: 'Development',
    skills: [
      'Java',
      'Spring Boot',
      'Python',
      'Django',
      'Angular',
      'React',
      'Flutter',
      'TypeScript'
    ]
  },
  {
    title: 'Data Engineering & DevOps',
    skills: [
      'PostgreSQL',
      'Docker',
      'Jenkins',
      'SonarQube',
      'Prometheus',
      'Grafana',
      'Git',
      'Linux'
    ]
  },
  {
    title: 'Databases',
    skills: [
      'PostgreSQL',
      'MySQL',
      'SQLite'
    ]
  },
  {
    title: 'Engineering',
    skills: [
      'Microservices',
      'REST APIs',
      'Agile Scrum',
      'TDD',
      'UML',
      'CI/CD'
    ]
  }
]
</script>

<template>
  <section id="skills" class="py-20 bg-gray-50 dark:bg-gray-900">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">

      <div class="text-center mb-12">
        <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white">
          Technical Skills
        </h2>

        <div class="w-20 h-1 bg-primary-600 mx-auto mt-4"></div>

        <p class="text-gray-600 dark:text-gray-300 mt-4 max-w-2xl mx-auto">
          A Data Science and AI foundation combined with hands-on experience
          in software development, data engineering and DevOps.
        </p>
      </div>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">

        <div
          v-for="category in skillCategories"
          :key="category.title"
          class="bg-white dark:bg-gray-800 p-6 rounded-xl shadow-sm"
        >
          <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-4">
            {{ category.title }}
          </h3>

          <div class="flex flex-wrap gap-2">

            <span
              v-for="skill in category.skills"
              :key="skill"
              class="px-3 py-2 bg-primary-50 dark:bg-gray-700 text-primary-700 dark:text-gray-200 rounded-lg text-sm"
            >
              {{ skill }}
            </span>

          </div>
        </div>

      </div>
    </div>
  </section>
</template>