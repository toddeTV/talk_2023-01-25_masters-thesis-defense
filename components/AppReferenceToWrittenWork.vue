<script setup lang="ts">
const props = defineProps({
  pages: {
    default: [],
  },
})
</script>

<template>
  <!-- TailwindCSS: amber-400 = #fbbf24 -->
  <div class="absolute top-0 right-14 z-20">
    <div class="flex flex-row justify-center bg-amber-400">
      <div class="flex flex-col pb-0.5 pt-1.5 font-bold space-y-0 text-sm">
        <span v-for="page in props.pages" class="text-center">
          {{ page }}
        </span>
      </div>
    </div>
    <div class="bookmark">
    </div>
  </div>
</template>

<style lang="css" scoped>
.bookmark{
  width: 44px;
  height: 25px;
  transform: rotate(0deg) skew(0deg);
  -webkit-transform: rotate(0deg) skew(0deg);
  border-left: 22px solid #fbbf24;
  border-right: 22px solid #fbbf24;
  border-bottom: 22px solid transparent;
}
</style>
