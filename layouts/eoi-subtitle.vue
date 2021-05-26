<script setup lang="ts">
import { defineProps } from 'vue'
const props = defineProps({
  items: {
    type: Array,
  }
})
</script>
<template>
  <div class="flex w-full h-full bg-center bg-cover menu" style="background-image: url(./images/bg-subtitle.png); align-items: center; justify-content: center">
    <v-click>
      <ul class="flex-col pl-20 pt-10 text-dark-900">
        <li class="flex w-100 h-14 pt-2 mb-10 bg-no-repeat bg-contain text-4xl" 
            style="background-image: url(./images/bg-subtitle-item.png)"
            v-for="(v, i) in items"
            :key="i">
          <i class="ml-5 mr-10 text-light-50">{{ i + 1}}</i>{{ v }}
        </li>
      </ul>
    </v-click>
  </div>
</template>
