<script setup lang="ts">
const certifications = [
  'IT Specialist — Artificial Intelligence · Certiport',
  'Building Transformer-Based NLP Applications · NVIDIA',
  'DLTC Blockchain Fundamentals · Dar Blockchain',
  'Hedera Certified Foundation · The Hashgraph Association',
  'Microsoft Certification · In Progress'
]
</script>

<template>
  <section id="certifications" class="py-20 bg-gray-50 dark:bg-gray-900">
    <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">

      <div class="text-center mb-12">
        <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white">
          Certifications
        </h2>

        <div class="w-20 h-1 bg-primary-600 mx-auto mt-4"></div>
      </div>

      <div class="grid md:grid-cols-2 gap-4">

        <div
          v-for="certification in certifications"
          :key="certification"
          class="bg-white dark:bg-gray-800 rounded-xl p-5 shadow-sm"
        >
          <p class="text-gray-700 dark:text-gray-200">
            {{ certification }}
          </p>
        </div>

      </div>
    </div>
  </section>
</template>