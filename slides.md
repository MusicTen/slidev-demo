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
# Web Component
<!--
这是备注
-->
---
layout: full-screen
image: ./images/bg-menu.png
---
<div>
  目录
</div>
<!--
这是备注
-->
---
layout: full-screen
image: ./images/bg-title-1.png
---

<div>
  标题样式1
  <v-click>

  Hello World

  </v-click>
  <v-clicks>

  - Item 1
  - Item 2
  - Item 3
  - Item 4

  </v-clicks>
</div>
<!--  -->
---
layout: full-screen
image: ./images/bg-title-2.png
---
<div>
  标题样式2

</div>
```ts {1-6}
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
```ts {monaco}
import { ref } from 'vue'
import { useMouse } from '@vueuse/core'

const counter = ref(0)
```
<!--  -->
---
layout: full-screen
image: ./images/bg-content-1.png
---
<div>
  内容样式1
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
