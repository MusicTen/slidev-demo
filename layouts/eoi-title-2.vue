<template>
  <div class="flex pt-40 pl-20 pr-30 w-full h-full bg-center bg-cover eoi-title-2"
       style="background-image: url(./images/bg-title-2.png)">
    <aside class="w-xs ml-10 text-6xl theme-color">📝定义</aside>
    <slot />
  </div>
</template>
<style>
.eoi-title-2 > div {
  flex: 1;
  display: flex;
  flex-direction: column;
}
</style>
