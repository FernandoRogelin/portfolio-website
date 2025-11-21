<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <section id="about" class="py-12 sm:py-16 md:py-20 px-4 sm:px-6 lg:px-8">
    <div class="max-w-4xl mx-auto">
      <h2
        class="text-3xl sm:text-4xl md:text-5xl font-bold text-center mb-8 sm:mb-12 bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent leading-normal"
        data-aos="fade-up"
      >
        {{ t('about.title') }}
      </h2>

      <div class="bg-white/5 backdrop-blur-lg rounded-2xl p-6 sm:p-8 border border-white/10" data-aos="fade-up" data-aos-delay="100">
        <p class="text-base sm:text-lg text-gray-300 leading-relaxed mb-6">
          {{ t('about.paragraph1') }}
        </p>

        <p class="text-base sm:text-lg text-gray-300 leading-relaxed mb-6">
          {{ t('about.paragraph2') }}
        </p>

        <p class="text-base sm:text-lg text-gray-300 leading-relaxed">
          {{ t('about.paragraph3') }}
        </p>
      </div>
    </div>
  </section>
</template>
