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
  <div class="flex flex-col pt-48px px-72px w-full h-full bg-center bg-cover style-one"
       :style="`background-image: url(${props.image})`">
    <h1 class="text-4xl font-bold mb-10">{{ props.title }}</h1>
    <slot />
  </div>
</template>
<style>
.style-one > div {
  flex: 1;
  display: flex;
  flex-direction: column;
}
</style>
