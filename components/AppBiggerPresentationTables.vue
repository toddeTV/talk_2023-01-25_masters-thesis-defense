<script setup lang="ts">
const props = defineProps({
  pages: {
    default: [],
  },
})
</script>

<template>
  <div v-if="$slidev.nav.clicks === 3">
    <img src="/assets/parameter-example-tables/2_one-table-with-overlap.png"
      v-click="3"
      class="animImg2 absolute bottom-40 left-20 z-10" />
    <img src="/assets/parameter-example-tables/3_multiple-tables-per-parameter.png"
        v-click="3"
        class="animImg2 absolute bottom-10 left-21 z-10" />
    <!-- <div v-click="3"
        class="absolute top-0 left-0 w-full h-full bg-white/75 z-1"></div> -->
    <div v-click="3"
        class="absolute top-75 left-0 w-127 h-25 bg-white z-1"></div>
    <div v-click="3"
        class="absolute top-109 left-0 w-127 h-18 bg-white z-1"></div>
    <div v-click="3"
        class="absolute top-99 left-30 w-127 h-18 bg-white z-1"></div>
  </div>
</template>

<style lang="css" scoped>
</style>
