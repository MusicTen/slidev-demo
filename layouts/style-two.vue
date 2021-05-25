<script setup lang="ts">
import { defineProps } from 'vue'
const props = defineProps({
  image: {
    type: String,
  },
  title: {
    type: String,
  }
})
</script>

<template>
  <div class="flex pt-40 pl-20 pr-30 w-full h-full bg-center bg-cover style-two"
       style="background-image: url('../images/bg-title-1.png')">
    <aside class="w-xs ml-10 text-6xl theme-color">📝定义</aside>
    <slot />
  </div>
</template>
<style>
.style-two > div {
  flex: 1;
  display: flex;
  flex-direction: column;
}
</style>
