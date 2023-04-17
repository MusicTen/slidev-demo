<script setup lang="ts">
defineProps({
  image: {
    type: String,
  },
})
</script>

<template>
  <div class="flex flex-col w-full h-full bg-center bg-cover full-screen"
       :style="`background-image: url(${image})`">
    <slot />
  </div>
</template>
<style>
.full-screen > div {
  flex: 1;
  display: flex;
  flex-direction: column;
}
</style>
