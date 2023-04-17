<script setup lang="ts">
defineProps({
  items: {
    type: Array,
  }
})
</script>
<template>
  <div class="flex flex-col w-full h-full bg-center bg-cover menu pl-80"
       style="background-image: url(../images/bg-menu.png); justify-content: center">
    <v-click>
      <ul class="mt-10">
        <li class="text-5xl font-bold mb-10 theme-color"
            v-for="(v, i) in items"
            :key="i">{{ v }}</li>
      </ul>
    </v-click>
  </div>
</template>
