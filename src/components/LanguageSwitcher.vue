<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { locale } = useI18n()

const changeLanguage = (lang: string) => {
  locale.value = lang
  localStorage.setItem('locale', lang)
}
</script>

<template>
  <div class="fixed top-6 right-6 z-50">
    <div class="flex gap-2 bg-white/10 backdrop-blur-lg rounded-full p-2 border border-white/20">
      <button
        @click="changeLanguage('en')"
        :class="[
          'px-4 py-2 rounded-full font-medium text-sm transition-all duration-300',
          locale === 'en'
            ? 'bg-gradient-to-r from-cyan-500 to-blue-500 text-white shadow-lg'
            : 'text-gray-300 hover:text-white hover:bg-white/10'
        ]"
      >
        EN
      </button>
      <button
        @click="changeLanguage('pt')"
        :class="[
          'px-4 py-2 rounded-full font-medium text-sm transition-all duration-300',
          locale === 'pt'
            ? 'bg-gradient-to-r from-cyan-500 to-blue-500 text-white shadow-lg'
            : 'text-gray-300 hover:text-white hover:bg-white/10'
        ]"
      >
        PT
      </button>
    </div>
  </div>
</template>
