<script setup lang="ts">
import { onMounted } from 'vue'
import AOS from 'aos'
import 'aos/dist/aos.css'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import ExperienceSection from './components/ExperienceSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import ContactSection from './components/ContactSection.vue'
import LanguageSwitcher from './components/LanguageSwitcher.vue'

onMounted(() => {
  AOS.init({
    duration: 1000,
    once: true,
    offset: 100,
  })
})
</script>

<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-900 via-slate-800 to-slate-900 text-white">
    <LanguageSwitcher />
    <HeroSection />
    <AboutSection />
    <ExperienceSection />
    <SkillsSection />
    <ProjectsSection />
    <ContactSection />
  </div>
</template>

<style>
html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  padding: 0;
}
</style>
