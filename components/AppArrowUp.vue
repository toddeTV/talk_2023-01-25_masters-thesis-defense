<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps({
  // left: {
  //   default: 0,
  // },
  nbr: {
    default: 0,
  },
})

const left = computed<number>(() => {
  if(props.nbr === 1)
    return 60
  if(props.nbr === 2)
    return 171
  if(props.nbr === 3)
    return 302
  if(props.nbr === 4)
    return 435
  if(props.nbr === 5)
    return 590
  if(props.nbr === 6)
    return 740
  return 0
})
</script>

<template>
  <div>
    <div class="mt-1" :style="'margin-left:'+left+'px;'">
      <!-- TailwindCSS gray-100 = #f3f4f6 -->
      <!-- TailwindCSS gray-200 = #e5e7eb -->
      <!-- TailwindCSS gray-400 = #9ca3af -->
      <svg width="100" height="30" class="-mb-0.5 z-10">
        <polygon points="30,5 60,50 0,50" style="fill:#e5e7eb;stroke:#9ca3af;stroke-width:2" />
      </svg>
    </div>
    <div class="border-t-2 border-gray-400 h-6 pb-1 bg-gradient-to-b from-gray-200 to-white -mb-2">
    </div>
  </div>
</template>

<style lang="css" scoped>
.gg-shape-triangle {
    position: relative;
    transform: scale(var(--ggs,1));
    width: 22px;
    height: 17px;
    border-left: 3px solid transparent;
    border-bottom: 3px solid
}
.gg-shape-triangle,
.gg-shape-triangle::before {
    display: block;
    box-sizing: border-box;
    border-right: 3px solid transparent
}
.gg-shape-triangle::before {
    content: "";
    position: absolute;
    width: 20px;
    height: 20px;
    border-left: 3px solid;
    border-top: 3px solid;
    border-bottom: 3px solid transparent;
    transform: rotate(45deg) skew(10deg,10deg);
    left: -2px;
    bottom: -13px
}
</style>
