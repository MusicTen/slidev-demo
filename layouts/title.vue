<script setup lang="ts">
import { defineProps } from 'vue'
const props = defineProps({
  title: {
    type: String,
  },
  subtitle: {
    type: String,
  }
})
</script>

<template>
  <div class="flex flex-col pt-50 pl-130 w-full h-full bg-center bg-cover style-one"
       :style="`background-image: url('./images/bg-title-2.png')`">
    <h1 class="text-4xl font-bold mb-20 theme-color">{{ props.title }}</h1>
    <h3 class="text-3xl theme-color ml-2">{{ props.subtitle }}</h3>
  </div>
</template>
