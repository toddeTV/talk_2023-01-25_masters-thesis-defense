<script setup lang="ts">
import { computed, ref } from 'vue'

const diagramDefaultStyle = [
  'top: 80px',
  'left: 15px',
  'width: 97%',
  'max-width: 97%',
]

const diagramStyles = computed(() => {
  if ($slidev.nav.clicks == 3)
    return [
      'top: -250px',
      'left: -950px',
      'width: 3000px',
      'max-width: 3000px',
    ]
  if ($slidev.nav.clicks == 4)
    return [
      'top: -90px',
      'left: -1050px',
      'width: 3600px',
      'max-width: 3600px',
    ]
  if ($slidev.nav.clicks == 5)
    return [
      'top: 30px',
      'left: 0px',
      'width: 3600px',
      'max-width: 3600px',
    ]
  return diagramDefaultStyle
})

const overlayStyles = computed(() => {
  if ($slidev.nav.clicks == 0 || $slidev.nav.clicks == 1 || $slidev.nav.clicks == 7)
    return [
      'opacity: 0.0',
    ]
  return [
    'opacity: 1.0',
  ]
})

const meme1Styles = computed(() => {
  if ($slidev.nav.clicks == 1 || $slidev.nav.clicks == 2)
    return [
      'opacity: 1.0',
    ]
  return [
    'opacity: 0.0',
  ]
})

const meme2Styles = computed(() => {
  if ($slidev.nav.clicks == 7)
    return [
      'opacity: 1.0',
    ]
  return [
    'opacity: 0.0',
  ]
})
</script>

<template>
  <div class="relative h-0 w-full">
    <!-- style="transform: translate(-50%, 0);" -->
    <img src="/assets/fmadb_uml/diagram1_fullSchema/prisma-erd-generator_manual-mermaid-1.svg"
         class="absolute transition-all duration-700 z-1"
         :style="[diagramStyles]"/>
    <img src="/assets/fmadb_uml/diagram1_fullSchema/prisma-erd-generator_manual-mermaid-1_colors.svg"
         class="absolute transition-all duration-700 z-2"
         :style="[diagramStyles, overlayStyles]"/>
    <img src="/assets/memes/what.jpg"
         class="absolute transition-all duration-700 z-2 w-40 right-40 top-60"
         :style="[meme1Styles]"/>
    <img src="/assets/memes/sense-now.jpg"
         class="absolute transition-all duration-700 z-2 w-40 right-40 top-60"
         :style="[meme2Styles]"/>
  </div>
</template>
