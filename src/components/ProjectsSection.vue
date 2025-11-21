<script setup lang="ts">
import { useI18n } from 'vue-i18n'
import { computed } from 'vue'

const { t } = useI18n()

interface Project {
  title: string
  company: string
  description: string
  technologies: string[]
  icon: string
}

const projects = computed<Project[]>(() => [
  {
    title: t('projects.items.deskbee.title'),
    company: t('projects.items.deskbee.company'),
    description: t('projects.items.deskbee.description'),
    technologies: ['VueJS', 'PHP', 'Laravel', 'Vite', 'TailwindCSS', 'Pinia', 'PlayWright', 'Datadog', 'MySQL', 'i18n'],
    icon: '🏢',
  },
  {
    title: t('projects.items.lumen.title'),
    company: t('projects.items.lumen.company'),
    description: t('projects.items.lumen.description'),
    technologies: ['React', 'C#', 'TypeScript', 'Jest', 'Zustand'],
    icon: '💼',
  },
  {
    title: t('projects.items.leste.title'),
    company: t('projects.items.leste.company'),
    description: t('projects.items.leste.description'),
    technologies: ['React', 'TypeScript', 'Performance Optimization', 'i18n'],
    icon: '🚀',
  },
])
</script>

<template>
  <section id="projects" class="py-20 px-4 sm:px-6 lg:px-8 bg-black/20">
    <div class="max-w-7xl mx-auto">
      <h2
        class="text-4xl sm:text-5xl font-bold text-center mb-16 bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent leading-normal"
        data-aos="fade-up"
      >
        {{ t('projects.title') }}
      </h2>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="(project, index) in projects"
          :key="index"
          class="group bg-white/5 backdrop-blur-lg rounded-2xl p-6 border border-white/10 hover:border-cyan-500/50 transition-all duration-300 hover:shadow-2xl hover:shadow-cyan-500/20 hover:-translate-y-2"
          data-aos="fade-up"
          :data-aos-delay="index * 100"
        >
          <!-- Project Icon -->
          <div class="text-5xl mb-4">{{ project.icon }}</div>

          <!-- Company Badge -->
          <div class="inline-block px-3 py-1 bg-cyan-500/20 text-cyan-300 rounded-full text-sm font-medium mb-3">
            {{ project.company }}
          </div>

          <!-- Project Title -->
          <h3 class="text-2xl font-bold text-white mb-3">{{ project.title }}</h3>

          <!-- Description -->
          <p class="text-gray-300 mb-6 leading-relaxed">{{ project.description }}</p>

          <!-- Technologies -->
          <div class="flex flex-wrap gap-2">
            <span
              v-for="(tech, techIndex) in project.technologies"
              :key="techIndex"
              class="px-3 py-1 bg-blue-500/10 text-blue-300 rounded-lg text-xs font-medium border border-blue-500/20"
            >
              {{ tech }}
            </span>
          </div>
        </div>
      </div>

      <!-- Additional Projects Note -->
      <div
        class="mt-12 text-center bg-gradient-to-r from-cyan-500/10 to-blue-500/10 backdrop-blur-lg rounded-2xl p-8 border border-cyan-500/20"
        data-aos="fade-up"
        data-aos-delay="300"
      >
        <p class="text-lg text-gray-300">
          {{ t('projects.footer') }}
        </p>
      </div>
    </div>
  </section>
</template>
