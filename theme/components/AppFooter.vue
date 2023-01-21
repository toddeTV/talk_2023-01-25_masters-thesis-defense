<script setup lang="ts">
import { computed } from 'vue'

defineProps({
  website: {
    type: String,
  },
})

const pageProcess = computed(() => {
  return Math.round((($slidev.nav.currentPage * 100) / $slidev.nav.total) * 100) / 100
})
</script>

<template>
  <footer class="flex flex-col justify-between w-full mt-auto text-blue-500 dark:text-white">
    <!-- infos: left website hyperlink and right the page number -->
    <div class="flex justify-between w-full text-blue-500 dark:text-white">
      <a v-if="website || $slidev.configs.author.website"
         :href="'https://' + (website || $slidev.configs.author.website)"
         target="_blank"
         class="mb-0 baseColor !border-b-0">
         <mdi-web class="baseColor mr-1" /> {{ website || $slidev.configs.author.website }}</a>
      <div>
        <span>{{ $slidev.nav.currentPage }}</span>
        <span v-if="$slidev.configs.themeConfig.showTotalPageCount"> / {{ $slidev.nav.total }}</span>
      </div>
    </div>

    <!-- progress bar -->
    <div v-if="$slidev.configs.themeConfig.showPageProcessBar" class="absolute bottom-0 left-0 w-full">
      <div class="w-full h-2">
        <div class="processColor h-2" :style="'width: '+pageProcess+'%'"></div>
      </div>
    </div>
  </footer>
</template>

<style lang="css" scoped>
.processColor{
    background-color: var(--slidev-theme-primary);
}
</style>
