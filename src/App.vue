<script setup lang="ts">
import TheNavbar from './components/TheNavbar.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import ExperienceSection from './components/ExperienceSection.vue'
import EducationSection from './components/EducationSection.vue'
import CertificationsSection from './components/CertificationsSection.vue'
import ContactSection from './components/ContactSection.vue'
</script>

<template>
  <div class="min-h-screen">

    <TheNavbar />

    <main>
      <HeroSection />

      <AboutSection />

      <SkillsSection />

      <ProjectsSection />

      <ExperienceSection />

      <EducationSection />

      <CertificationsSection />

      <ContactSection />
    </main>

  </div>
</template>