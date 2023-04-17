<script setup lang="ts">
defineProps({
  title: {
    type: String,
  },
  subtitle: {
    type: String,
  }
})
</script>

<template>
  <div class="flex flex-col pt-50 pl-130 w-full h-full bg-center bg-cover"
       style="background-image: url(./images/bg-title-1.png)">
    <h1 class="text-4xl font-bold mb-16 theme-color">{{ title }}</h1>
    <h3 class="text-3xl theme-color">{{ subtitle }}</h3>
  </div>
</template>
