---
# try also 'default' to start simple
theme: default
# # random image from a curated Unsplash collection by Anthony
# # like them? see https://unsplash.com/collections/94734566/slidev
background: ./images/bg-home-page.png
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.
  Learn more at [Sli.dev](https://sli.dev)
---
# Web Component
---
layout: full-screen
image: ./images/bg-home-page.png
---
<div class="mt-30 ml-50 text-gray-100">
  <h1 class="text-4xl font-bold mb-10">Web Components</h1>
  <p class="text-2xl">分享人：王璨</p>
</div>
<!--
这是备注
-->
---
layout: full-screen
image: ./images/bg-content-2.png
---
<div class="mt-12 ml-20 relative">
  <h1 class="text-3xl font-bold mb-10">引言</h1>
  <v-clicks>

  - <p class="mb-4">通常一个应用会以一棵嵌套的组件树（DOM tree）的形式来组织；</p>
  - <p class="mb-4">web组件 = html + css + js</p>
  - <p class="mb-4">组件特点：高内聚低耦合</p>
  - <p class="mb-4">拆分组件原则：可维护性+复用性</p>

  </v-clicks>
  <img v-click v-motion
    :initial="{ x: -80, opacity: 0}"
    :enter="{ x: 0, opacity: 1, transition: { delay: 2000, duration: 1000 } }"     class="w-screen-sm absolute right-10px top-150px" src="https://cn.vuejs.org/images/components.png" />
</div>
---
layout: full-screen
image: ./images/bg-content-2.png
---
<div class="mt-12 ml-20">
  <h1 class="text-3xl font-bold mb-10">引言</h1>
  <p class="mb-4">组件是前端的发展方向，现在流行的 React 和 Vue 都是组件框架。</p>
  <a class="mb-4" href="https://react.docschina.org/docs/components-and-props.html">react组件：</a>
  <p class="mb-4" v-click>函数组件与 class 组件 => UI = f(data)</p>
  <a class="mb-4" href="https://v3.cn.vuejs.org/guide/component-basics.html">vue3组件：</a>
  <p class="mb-8" v-click>vue单文件组件</p>
  <p v-click>谷歌公司由于掌握了 Chrome 浏览器，一直在推动浏览器的原生组件，即 Web Components API。</p>
  <p v-after>相比第三方框架，原生组件简单直接，符合直觉，不用加载任何外部模块，代码量小。</p>
</div>
---
layout: full-screen
image: ./images/bg-menu.png
---
<style>
  .theme-color {
    color: #00c8c1;
  }
</style>
<div class="flex mt-20">
  <aside class="ml-15 mr-50 text-5xl text-gray-200">目录</aside>
  <ul class="mt-10">
    <li v-click class="text-5xl font-bold mb-10 theme-color">web components介绍</li>
    <li v-after class="text-5xl font-bold mb-10 theme-color">web components运用</li>
    <li v-after class="text-5xl font-bold mb-10 theme-color">第三方封装库</li>
    <li v-after class="text-5xl font-bold theme-color">总结</li>
  </ul>
</div>
<!--
这是备注
-->
---
layout: full-screen
image: ./images/bg-title-2.png
---
<style>
  .theme-color {
    color: #00c8c1;
  }
</style>
<div class="ml-130 mt-50 font-bold theme-color">
  <h1 v-motion
      :initial="{ x: -80 }"
      :enter="{ x: 0 }"
      class="text-5xl mb-10">
    Web Components
  </h1>
  <p class="text-3xl ml-2">介绍</p>
</div>
---
layout: full-screen
image: ./images/bg-title-1.png
---
<style>
  .theme-color {
    color: #00c8c1;
  }
</style>
<div class="flex mt-30">
  <aside class="w-xs ml-30 mr-40 text-6xl theme-color">定义</aside>
  <div class="pt-10 pr-22">Web Components 是一套不同的技术，允许您创建可重用的定制元素（它们的功能封装在您的代码之外）并且在您的web应用中使用它们。—— MDN</div>
</div>
<!--  -->
---
layout: full-screen
image: ./images/bg-content-2.png
---
<div class="mt-12 ml-20">
  <h1 class="text-3xl font-bold mb-10">目标</h1>
</div>

```html {6-8}
  <!DOCTYPE html>
  <html lang="en">
      <head>
          <title>web components</title>
      </head>
      <body>
          <my-button></my-button>
      </body>
  </html>
```
<!--  -->
---
layout: image
image: ./images/bg-content-1.png
---
<div class="theme-color">
  <h2 class="mb-10">Web Components主要由三项技术组成，分别为</h2>
  <p class="ml-10 font-bold">1. Custom elements（自定义元素）</p>
  <p class="ml-10 font-bold">2. Shadow DOM（影子DOM）</p>
  <p class="ml-10 font-bold">3. HTML templates（HTML模板）</p>
  <p class="mt-10">它们可以一起使用来创建功能强大的定制元素，并且可以在我们喜欢的任何地方重用，不必担心代码冲突。</p>
</div>
---
layout: full-screen
image: ./images/bg-content-2.png
---
<div>
  内容样式2
</div>
<!--  -->
---
layout: full-screen
image: ./images/bg-end.png
---
<div>
  结束
</div>
<!--  -->
---
