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
layout: menu
---
<style>
  .theme-color {
    color: #00c8c1;
  }
</style>
---
layout: style-one
image: ./images/bg-content-2.png
title: '123'
---
<div>
  内容
</div>

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
layout: style-one
image: ./images/bg-content-2.png
title: '引言'
---
<div class="">
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
layout: style-one
image: ./images/bg-content-2.png
title: '引言'
---
<div class="">
  <p class="mb-4">组件是前端的发展方向，现在流行的 React 和 Vue 都是组件框架。</p>
  <a class="mb-4" href="https://react.docschina.org/docs/components-and-props.html">react组件：</a>
  <p class="mb-4 text-rose-600" v-click>函数组件与 class 组件 => UI = f(data)</p>
  <a class="mb-4" href="https://v3.cn.vuejs.org/guide/component-basics.html">vue3组件：</a>
  <p class="mb-8 text-rose-600" v-click>vue单文件组件</p>
  <p v-click>谷歌公司由于掌握了 Chrome 浏览器，一直在推动浏览器的原生组件，即 Web Components API。</p>
  <p v-after>相比第三方框架，原生组件简单直接，符合直觉，不用加载任何外部模块，代码量小。</p>
</div>
---
layout: menu
---
<ul class="mt-10">
  <li v-click class="text-5xl font-bold mb-10 theme-color">web components介绍</li>
  <li v-after class="text-5xl font-bold mb-10 theme-color">web components运用</li>
  <li v-after class="text-5xl font-bold mb-10 theme-color">第三方封装库</li>
  <li v-after class="text-5xl font-bold theme-color">总结</li>
</ul>
<!--
这是备注
-->
---
layout: title
title: Web Components
subtitle: 介绍
---
---
layout: style-two
image: ./images/bg-title-1.png
title: 定义
---
<div class="text-light-50 text-xl">Web Components 是一套不同的技术，允许您创建可重用的定制元素（它们的功能封装在您的代码之外）并且在您的web应用中使用它们。—— MDN</div>
<!--  -->
---
layout: style-one
image: ./images/bg-content-2.png
title: 目标
---

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
image: ./images/bg-subtitle.png
---
<style>
  .subtitle {
    list-style: none;
    background-image: url('./images/bg-subtitle-item.png')
  }
</style>
<ul class="pl-70 pt-10 text-dark-900">
  <li class="w-200 h-14 mb-10 bg-no-repeat bg-contain subtitle text-3xl"
      v-for="(v, i) in ['注册与使用', '组件通信', '组件生命周期', '组件插槽']" :key="i">
    <i class="ml-4 mr-10 text-light-50">{{ i + 1}}</i>{{ v }}
  </li>
</ul>
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
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# Code

Use code snippets and get the highlighting directly!

```ts {all|2|1-6|9|all}
interface User {
  id: number
  firstName: string
  lastName: string
  role: string
}

function updateUser(id: number, update: User) {
  const user = getUser(id)
  const newUser = {...user, ...update}
  saveUser(id, newUser)
}
```

<arrow v-click="3" x1="400" y1="420" x2="230" y2="330" color="#564" width="3" arrowSize="1" />
---
layout: full-screen
image: './images/bg-content-2.png'
---
<div>
  内容样式2
</div>
<!--  -->
---
layout: full-screen
image: './images/bg-end.png'
---