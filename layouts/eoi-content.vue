<script setup lang="ts">
import { defineProps } from 'vue'
const props = defineProps({
  title: {
    type: String,
  }
})
</script>

<template>
  <div class="flex flex-col pt-48px px-72px w-full h-full bg-center bg-cover"
       style="background-image: url(./images/bg-content.png);">
    <h1 class="text-4xl font-bold pl-2 mb-8">{{ title }}</h1>
    <slot />
  </div>
</template>
