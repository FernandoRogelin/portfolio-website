<script setup lang="ts">
import { useI18n } from 'vue-i18n'
import { computed } from 'vue'

const { t } = useI18n()

interface SkillCategory {
  title: string
  skills: string[]
  icon: string
}

const skillCategories = computed<SkillCategory[]>(() => [
  {
    title: t('skills.categories.languages'),
    icon: '💻',
    skills: ['JavaScript', 'TypeScript', 'HTML5', 'CSS3', 'NodeJS', 'PHP', 'MySQL'],
  },
  {
    title: t('skills.categories.frameworks'),
    icon: '⚡',
    skills: [
      'React',
      'NextJS',
      'Remix',
      'Redux',
      'Zustand',
      'VueJS (2, 3)',
      'Vuex',
      'Pinia',
      'Laravel',
      'Express',
      'Koa',
    ],
  },
  {
    title: t('skills.categories.uiStyling'),
    icon: '🎨',
    skills: [
      'TailwindCSS',
      'Styled-components',
      'Emotion',
      'Shadcn',
      'Shadcn-vue',
      'Quasar',
      'Vuetify',
    ],
  },
  {
    title: t('skills.categories.testing'),
    icon: '🧪',
    skills: ['Jest', 'Vitest', 'Cypress', 'Testing Library', 'PlayWright'],
  },
  {
    title: t('skills.categories.tools'),
    icon: '🔧',
    skills: ['Git', 'Webpack', 'Vite', 'Storybook', 'Husky', 'Prettier', 'ESLint'],
  },
  {
    title: t('skills.categories.cloud'),
    icon: '☁️',
    skills: ['Azure', 'Azure Pipeline', 'Datadog', 'Grafana Faro'],
  },
  {
    title: t('skills.categories.methodologies'),
    icon: '📋',
    skills: [
      'Agile',
      'Scrum',
      'TDD',
      'Flux Architecture',
      'Clean Architecture',
      'Core Web Vitals',
    ],
  },
  {
    title: t('skills.categories.i18n'),
    icon: '🌍',
    skills: ['i18n', 'Vue-gettext'],
  },
])
</script>

<template>
  <section id="skills" class="py-20 px-4 sm:px-6 lg:px-8">
    <div class="max-w-7xl mx-auto">
      <h2
        class="text-4xl sm:text-5xl font-bold text-center mb-16 bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent leading-normal"
        data-aos="fade-up"
      >
        {{ t('skills.title') }}
      </h2>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">
        <div
          v-for="(category, index) in skillCategories"
          :key="index"
          class="bg-white/5 backdrop-blur-lg rounded-2xl p-6 border border-white/10 hover:border-cyan-500/50 transition-all duration-300 hover:shadow-xl hover:shadow-cyan-500/10 hover:scale-105"
          data-aos="fade-up"
          :data-aos-delay="index * 50"
        >
          <!-- Category Header -->
          <div class="flex items-center gap-3 mb-4">
            <span class="text-3xl">{{ category.icon }}</span>
            <h3 class="text-xl font-bold text-white">{{ category.title }}</h3>
          </div>

          <!-- Skills List -->
          <div class="flex flex-wrap gap-2">
            <span
              v-for="(skill, skillIndex) in category.skills"
              :key="skillIndex"
              class="px-3 py-1.5 bg-cyan-500/10 text-cyan-300 rounded-lg text-sm font-medium border border-cyan-500/20 hover:bg-cyan-500/20 transition-colors"
            >
              {{ skill }}
            </span>
          </div>
        </div>
      </div>

      <!-- Additional Info -->
      <div
        class="mt-12 text-center bg-white/5 backdrop-blur-lg rounded-2xl p-8 border border-white/10"
        data-aos="fade-up"
        data-aos-delay="300"
      >
        <p class="text-lg text-gray-300">
          {{ t('skills.footer') }}
        </p>
      </div>
    </div>
  </section>
</template>
