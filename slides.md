---
# try also 'default' to start simple
theme: default
# # random image from a curated Unsplash collection by Anthony
# # like them? see https://unsplash.com/collections/94734566/slidev
background: ./images/bg-home.png
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

<style>
  .theme-color {
    color: #00c8c1;
  }
</style>

# Web Components

---
layout: full-screen
image: ./images/bg-home.png
---

<div class="mt-30 ml-50 text-gray-100">
  <h1 class="text-4xl font-bold mb-10">Web Components</h1>
  <p class="text-2xl">分享人：王璨</p>
</div>

---
layout: eoi-content
title: 引言
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
layout: eoi-content
title: 引言
---

<div>
  <p class="mb-4">组件是前端的发展方向，现在流行的 React 和 Vue 都是组件框架。</p>
  <a href="https://react.docschina.org/docs/components-and-props.html">react组件：</a>
  <p class="ml-8 mt-6 mb-8 text-rose-600" v-click>函数组件与 class 组件 => UI = f(data)</p>
  <a href="https://v3.cn.vuejs.org/guide/component-basics.html">vue3组件：</a>
  <p class="ml-8 mt-6 mb-8 text-rose-600" v-click>vue单文件组件</p>
  <p v-click>谷歌公司由于掌握了 Chrome 浏览器，一直在推动浏览器的原生组件，即 Web Components API。</p>
  <p v-after>相比第三方框架，原生组件简单直接，符合直觉，不用加载任何外部模块，代码量小。</p>
</div>

---
layout: eoi-menu
items: [
  'web components介绍',
  'web components运用',
  '第三方封装库',
  '总结'
]
---
layout: eoi-title-1
title: Web Components
subtitle: 介绍
---
layout: eoi-title-2
title: 定义
---

<div class="text-light-50 text-xl">Web Components 是一套不同的技术，允许您创建可重用的定制元素（它们的功能封装在您的代码之外）并且在您的web应用中使用它们。—— MDN</div>
<!--  -->

---
layout: eoi-content
title: 目标
---

```html {6-14}
  <!DOCTYPE html>
  <html lang="en">
      <head>
          <title>web components</title>
      </head>
      <body>
          <v-page>
            <v-header>标题<v-header>
            <v-content>
              <v-aside>侧边栏</v-aside>
              <v-main>内容区域</v-main>
            </v-content>
          </v-page>
      </body>
  </html>
```
<!--  -->

---
layout: eoi-content
title: 技术依赖
---

<div class="theme-color">
  <h2 class="mb-10">Web Components主要由三项技术组成，分别为</h2>
  <p class="ml-10 mb-4 font-bold">1. Custom elements（自定义元素）</p>
  <p class="ml-10 mb-4 font-bold">2. Shadow DOM（影子DOM）</p>
  <p class="ml-10 mb-4 font-bold">3. HTML templates（HTML模板）</p>
  <p class="mt-10">它们可以一起使用来创建功能强大的定制元素，并且可以在我们喜欢的任何地方重用，不必担心代码冲突。</p>
</div>

---
layout: eoi-title-1
title: Web Components
subtitle: 使用
---
layout: eoi-subtitle
items: [
  '注册与使用',
  '组件插槽',
  '组件生命周期',
  '组件通信',
]
---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# customElements

自定义标签

```js
// 注册
customElements.define('my-button', MyButton, extends);
```
- name 所创建的元素名称，且需符合 DOMString 标准的字符串。注意，custom element 的名称不能是单个单词，且其中必须要有短横线
- class 用于定义元素行为的类
- extends 可选参数，一个包含 extends 属性的配置对象，指定了所创建的元素继承自哪个内置元素，可以继承任何内置元素。
---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# Shadow DOM

将一个隐藏的、独立的 DOM附加到一个元素上，并且允许将隐藏的 DOM 树附加到常规的 DOM 树中

```js
class MyButton extends HTMLElement {
  constructor() {
    super();
    // 第一步：创建组件根节元素：shadom DOM节点
    const shadow = this.attachShadow({ mode: 'open' });
    // 第二步：向shadom DOM添加内容
    shadowRoot.innerHTML = `
      <style>
        button {
          color: #fff;
          background-color: #ccc;
        }
      </style>
      <button>自定义按钮</button>
    `;
  }
}
```

---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# template

自定义模板，替代字符串模板

```html {all|2|1-6|9|all}
<template id="template">
  <style>
    button {
      color: #fff;
      background-color: #ccc;
    }
  </style>
  <button>自定义按钮</button>
</template>
```

---
layout: eoi-content
title: 生命周期
---

- connectedCallback：当 custom element首次被插入文档DOM时，被调用

- disconnectedCallback：当 custom element从文档DOM中删除时，被调用

- adoptedCallback：当 custom element被移动到新的文档时，被调用

- attributeChangedCallback: 当 custom element增加、删除、修改自身属性时，被调用

---
layout: eoi-content
title: 组件通信

---
```html {all|7-13|17-18|all}
  <script>
    class MyButton extends HTMLElement {
      constructor() {
        super();
        ...
        this.$button = shadow.querySelector('button');
        this.$button.addEventListener('click', () => {
          // 抛出事件
          this.dispatchEvent(new CustomEvent('custom', {
            detail: {message: '123'},
            // composed: true
          }));
        });
      }
    }
    customElements.define('my-button', MyButton);
    const btn = document.querySelector('my-button');
    btn.addEventListener('custom', e => console.log(e.detail.message));
  </script>
```

---
layout: eoi-title-1
title: 第三方封装库
subtitle: lit / lit-element / vue-lit
---
layout: eoi-content
title: lit
---

<div>
  <p class="text-2xl">谷歌开发，之前是 polymer，现在是 lit</p>
  <p>lit 完全包含 lit-element，lit-html</p>
  <p>lit-element 是对原生自定义组件的一次封装 lit-element 是一个可以创建 Web Component 的 base class，可以理解成 jQuery 相对于 js</p>
  <p>lit-html 是 lit-element 依赖的HTML模板引擎 vue-lit 是尤雨溪在去年9月，基于 vue3 核心包 @vue/reactivity 配合 lit-html 开发的一个可以直接在浏览器中渲染 vue 写法的 Web Component 的工具（70行代码）</p>
</div>

---
layout: eoi-content
title: lit-html
---

```js {all|1|2-17|12-16|18|all}
import { html, render } from 'lit-html';
const Button = (text, props = { type: 'default', borderRadius: '2px' }, onClick) => {
  const clickHandler = {
    handleEvent(e) {
      alert('inner clicked!');
      if (onClick) {
        onClick();
      }
    },
    capture: true,
  };
  return html`
    <button class="btn btn-${props.type}" @click=${clickHandler}>
      ${text}
    </button>
  `
};
render(Button('Defualt'), document.getElementById('button1'));
```
---
layout: eoi-content
title: vue-lit
---

```html {all|4|6|7-17|all}
<!DOCTYPE html>
<html lang="en">
  <body>
    <my-component />
    <script type="module">
      import { defineComponent, reactive, html, onMounted } from 'https://unpkg.com/@vue/lit';
      defineComponent('my-component', () => {
        const state = reactive({ text: 'Hello World' });
        function onClick() {  alert('cliked!') }
        onMounted(() => console.log('mounted'));
        return () => html`
          <p>
            <button @click=${onClick}>Click me</button>
            ${state.text}
          </p>
        `;
      })
    </script>
  </body>
</html>
```
---
layout: eoi-title-1
title: 总结
---
layout: eoi-content
title: 总结
---

<div>
  <p>创建一个类或函数来指定web组件的功能，如果使用类，请使用 ES6 的类语法。</p>
  <p>使用 CustomElementRegistry.define 方法注册您的自定义元素 ，并向其传递要定义的元素名称、指定元素功能的类、以及可选的其所继承自的元素。</p>
  <p>如果需要的话，使用 Element.attachShadow 方法将一个 shadow DOM 附加到自定义元素上。使用通常的 DOM 方法向  shadow DOM 中添加子元素、事件监听器等。</p>
  <p>如果需要的话，使用 template 和 slot 定义一个HTML 模板。再次使用常规DOM方法克隆模板并将其附加到您的 shadow DOM 中。</p>
  <p>在页面任何位置使用自定义元素，就像使用常规 HTML 元素那样。</p>
</div>

---
layout: full-screen
image: './images/bg-end.png'
---
