<script setup lang="ts">
import { useI18n } from 'vue-i18n'
import { computed } from 'vue'

const { t, tm } = useI18n()

interface Experience {
  company: string
  position: string
  period: string
  location: string
  achievements: string[]
}

const experiences = computed<Experience[]>(() => [
  {
    company: t('experience.companies.deskbee.name'),
    position: t('experience.companies.deskbee.position'),
    period: t('experience.companies.deskbee.period'),
    location: t('experience.companies.deskbee.location'),
    achievements: tm('experience.companies.deskbee.achievements') as string[],
  },
  {
    company: t('experience.companies.usabit.name'),
    position: t('experience.companies.usabit.position'),
    period: t('experience.companies.usabit.period'),
    location: t('experience.companies.usabit.location'),
    achievements: tm('experience.companies.usabit.achievements') as string[],
  },
])
</script>

<template>
  <section id="experience" class="py-20 px-4 sm:px-6 lg:px-8 bg-black/20">
    <div class="max-w-6xl mx-auto">
      <h2
        class="text-4xl sm:text-5xl font-bold text-center mb-16 bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent leading-normal"
        data-aos="fade-up"
      >
        {{ t('experience.title') }}
      </h2>

      <div class="relative">
        <!-- Timeline Line -->
        <div class="hidden md:block absolute left-1/2 transform -translate-x-1/2 h-full w-0.5 bg-gradient-to-b from-cyan-500 to-blue-500"></div>

        <!-- Experience Items -->
        <div class="space-y-12">
          <div
            v-for="(exp, index) in experiences"
            :key="index"
            class="relative"
            data-aos="fade-up"
            :data-aos-delay="index * 100"
          >
            <!-- Timeline Dot -->
            <div class="hidden md:block absolute left-1/2 transform -translate-x-1/2 -translate-y-4">
              <div class="w-4 h-4 rounded-full bg-gradient-to-r from-cyan-500 to-blue-500 ring-4 ring-slate-900"></div>
            </div>

            <!-- Experience Card -->
            <div :class="[
              'md:w-1/2',
              index % 2 === 0 ? 'md:mr-auto md:pr-8' : 'md:ml-auto md:pl-8'
            ]">
              <div class="bg-white/5 backdrop-blur-lg rounded-2xl p-6 border border-white/10 hover:border-cyan-500/50 transition-all duration-300 hover:shadow-xl hover:shadow-cyan-500/10">
                <!-- Company & Position -->
                <div class="mb-4">
                  <h3 class="text-2xl font-bold text-cyan-400 mb-1">{{ exp.company }}</h3>
                  <p class="text-xl text-white font-semibold mb-2">{{ exp.position }}</p>
                  <div class="flex flex-col sm:flex-row sm:items-center gap-2 text-gray-400 text-sm">
                    <span class="flex items-center gap-1">
                      <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
                      </svg>
                      {{ exp.period }}
                    </span>
                    <span class="hidden sm:block">•</span>
                    <span class="flex items-center gap-1">
                      <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                      </svg>
                      {{ exp.location }}
                    </span>
                  </div>
                </div>

                <!-- Achievements -->
                <ul class="space-y-3">
                  <li
                    v-for="(achievement, aIndex) in exp.achievements"
                    :key="aIndex"
                    class="flex items-start gap-2 text-gray-300"
                  >
                    <svg class="w-5 h-5 text-cyan-500 mt-0.5 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                    </svg>
                    <span class="break-words leading-relaxed">{{ achievement }}</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
