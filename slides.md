---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
---

# Welcome to Slidev

Presentation slides for developers

<div class="pt-12">
  <span @click="$slidev.nav.next" class="rounded cursor-pointer py-1 px-2" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="flex m-6 gap-2 abs-br">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl opacity-50 icon-btn !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl opacity-50 icon-btn !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
clicks: 8
---

# Que es una aplicación web?

Una aplicación web es un programa que se almacena en un servidor remoto y se entrega a través de la interfaz de navegador.

<div class="flex flex-col absolute items-center">
  <h2 v-click="3" class="text-gray-600 !text-xl">CLIENTE</h2>
  <p v-click="3" class="text-gray-600 !my-1">frontend</p>
  <img v-click="3" src="/frontend.png" class="h-26">
  <ul v-click="4" class="mt-4 text-sm text-gray-500">
    <li><logos-html5 /> HTML</li>
    <li><logos-css3 /> CSS</li>
    <li><logos-javascript /> JavaScript</li>
    <li><logos-vue /> Vue.js</li>
    <li><logos-vitejs /> Vite</li>
  </ul>
</div>

<div class="flex flex-col left-124 absolute items-center">
  <h2 v-click="1" class="text-gray-600 !text-xl">SERVIDOR</h2>
  <p v-click="1" class="text-gray-600 !my-1">backend</p>
  <img v-click="1" src="/backend.png" class="h-28">
  <ul v-click="2" class="mt-4 text-sm text-gray-500">
    <li><logos-go /> Go</li>
    <li><logos-jwt-icon /> JWT</li>
    <li><logos-oracle /> Oracle</li>
    <li><logos-mongodb /> MongoDB</li>
    <li><logos-docker-icon /> docker</li>
  </ul>
</div>
<img v-click="6" src="/database.png" class="h-28 top-62 left-200 absolute">

<arrow v-click="5" x1="260" y1="260" x2="480" y2="260" color="#55c" width="2" />
<p v-click="5" class="h-26 text-xs top-62 left-65 text-gray-400 absolute">http://xp25/ifs/ot/active?planta=2000</p>
<arrow v-click="6" x1="620" y1="260" x2="780" y2="260" color="#55c" width="2" />
<p v-click="6" class="h-26 text-xs top-62 left-155 text-gray-400 absolute">SELECT * FROM active_work...</p>

<arrow v-click="7" x2="620" y2="320" x1="780" y1="320" color="#55c" width="2" />
<arrow v-click="8" x2="260" y2="320" x1="480" y1="320" color="#55c" width="2" />

<pre v-click="8" class="text-xs top-80 left-70 text-gray-400 absolute">
[
  { ot: 123450,
    componente: 'TL91L001',
    planta: 2000,
    ...
  },
  { ot: 640361, ... },
  { ot: 124876, ... },
  { ot: 168701, ... },
]
</pre>

<style>
h1 {
  margin-top: 1rem;
  margin-bottom: 2rem;
}
</style>
---

# Fases de desarrollo de software

La metodología para el desarrollo de software es un modo sistemático de realizar, gestionar y administrar un proyecto para llevarlo a cabo con grandes posibilidades de éxito. Esta sistematización indica cómo se divide un proyecto en módulos más pequeños para normalizar cómo se administra el mismo.

<h4 v-click="1" class="py-4">Modelo en cascada</h4>

<div v-click="1" class="border-red-800 border-2 text-sm p-2 text-red-800 absolute">
  Planificación
</div>
<div v-click="1" class="border-orange-600 border-2 text-sm p-2 transform text-orange-600 translate-y-12 translate-x-14 absolute">
  Análisis
</div>
<div v-click="1" class="border-green-500 border-2 text-sm p-2 transform text-green-500 translate-y-24 translate-x-28 absolute">
  Diseño
</div>
<div v-click="1" class="border-gray-700 border-2 text-sm p-2 transform text-gray-700 translate-y-36 translate-x-42 absolute">
  Implementación
</div>
<div v-click="1" class="border-blue-500 border-2 text-sm p-2 transform text-blue-500 translate-y-48 translate-x-56 absolute">
  Verificación
</div>

<arrow v-click="1" x2="250" y2="460" x1="60" y1="290" color="#55c" width="2" />

<img v-click="2" src="/sdlc.png" class="transform w-64 translate-x-120">
---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# Code

Use code snippets and get the highlighting directly![^1]

```ts {all|2|1-6|9|all}
interface User {
  id: number
  firstName: string
  lastName: string
  role: string
}

function updateUser(id: number, update: User) {
  const user = getUser(id)
  const newUser = { ...user, ...update }
  saveUser(id, newUser)
}
```

<arrow v-click="3" x1="400" y1="420" x2="230" y2="330" color="#564" width="3" arrowSize="1" />

[^1]: [Learn More](https://sli.dev/guide/syntax.html#line-highlighting)

<style>
.footnotes-sep {
  @apply mt-20 opacity-10;
}
.footnotes {
  @apply text-sm opacity-75;
}
.footnote-backref {
  display: none;
}
</style>

---

# Components

<div grid="~ gap-4 cols-2">
<div>

You can use Vue components directly inside your slides.

We have provided a few built-in components like `<Tweet/>` and `<Youtube/>` that you can use directly. And adding your custom components is also super easy.

```html
<Counter :count="10" />
```

<!-- ./components/Counter.vue -->
<Counter :count="10" m="t-4" />

Check out [the guides](https://sli.dev/builtin/components.html) for more.

</div>
<div>

```html
<Tweet id="1390115482657726468" />
```

<Tweet id="1390115482657726468" scale="0.65" />

</div>
</div>


---
class: px-20
---

# Themes

Slidev comes with powerful theming support. Themes can provide styles, layouts, components, or even configurations for tools. Switching between themes by just **one edit** in your frontmatter:

<div grid="~ gap-2 cols-2" m="-t-2">

```yaml
---
theme: default
---
```

```yaml
---
theme: seriph
---
```

<img border="rounded" src="https://github.com/slidevjs/themes/blob/main/screenshots/theme-default/01.png?raw=true">

<img border="rounded" src="https://github.com/slidevjs/themes/blob/main/screenshots/theme-seriph/01.png?raw=true">

</div>

Read more about [How to use a theme](https://sli.dev/themes/use.html) and
check out the [Awesome Themes Gallery](https://sli.dev/themes/gallery.html).

---
preload: false
---

# Animations

Animations are powered by [@vueuse/motion](https://motion.vueuse.org/).

```html
<div
  v-motion
  :initial="{ x: -80 }"
  :enter="{ x: 0 }">
  Slidev
</div>
```

<div class="mt-6 w-60 relative">
  <div class="h-40 w-40 relative">
    <img
      v-motion
      :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
      :enter="final"
      class="top-0 right-0 bottom-0 left-0 absolute"
      src="https://sli.dev/logo-square.png"
    />
    <img
      v-motion
      :initial="{ y: 500, x: -100, scale: 2 }"
      :enter="final"
      class="top-0 right-0 bottom-0 left-0 absolute"
      src="https://sli.dev/logo-circle.png"
    />
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 2, rotate: 100 }"
      :enter="final"
      class="top-0 right-0 bottom-0 left-0 absolute"
      src="https://sli.dev/logo-triangle.png"
    />
  </div>

  <div
    class="top-14 left-40 text-5xl text-[#2B90B6] -z-1 absolute"
    v-motion
    :initial="{ x: -80, opacity: 0}"
    :enter="{ x: 0, opacity: 1, transition: { delay: 2000, duration: 1000 } }">
    Slidev
  </div>
</div>

<!-- vue script setup scripts can be directly used in markdown, and will only affects current page -->
<script setup lang="ts">
const final = {
  x: 0,
  y: 0,
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

<div
  v-motion
  :initial="{ x:35, y: 40, opacity: 0}"
  :enter="{ y: 0, opacity: 1, transition: { delay: 3500 } }">

[Learn More](https://sli.dev/guide/animations.html#motion)

</div>

---

# LaTeX

LaTeX is supported out-of-box powered by [KaTeX](https://katex.org/).

<br>

Inline $\sqrt{3x-1}+(1+x)^2$

Block
$$
\begin{array}{c}

\nabla \times \vec{\mathbf{B}} -\, \frac1c\, \frac{\partial\vec{\mathbf{E}}}{\partial t} &
= \frac{4\pi}{c}\vec{\mathbf{j}}    \nabla \cdot \vec{\mathbf{E}} & = 4 \pi \rho \\

\nabla \times \vec{\mathbf{E}}\, +\, \frac1c\, \frac{\partial\vec{\mathbf{B}}}{\partial t} & = \vec{\mathbf{0}} \\

\nabla \cdot \vec{\mathbf{B}} & = 0

\end{array}
$$

<br>

[Learn more](https://sli.dev/guide/syntax#latex)

---

# Diagrams

You can create diagrams / graphs from textual descriptions, directly in your Markdown.

<div class="-mb-6 grid pt-4 gap-10 grid-cols-3">

```mermaid {scale: 0.5}
sequenceDiagram
    Alice->John: Hello John, how are you?
    Note over Alice,John: A typical interaction
```

```mermaid {theme: 'neutral', scale: 0.8}
graph TD
B[Text] --> C{Decision}
C -->|One| D[Result 1]
C -->|Two| E[Result 2]
```

```plantuml {scale: 0.7}
@startuml

package "Some Group" {
  HTTP - [First Component]
  [Another Component]
}

node "Other Groups" {
  FTP - [Second Component]
  [First Component] --> FTP
}

cloud {
  [Example 1]
}


database "MySql" {
  folder "This is my folder" {
    [Folder 3]
  }
  frame "Foo" {
    [Frame 4]
  }
}


[Another Component] --> [Example 1]
[Example 1] --> [Folder 3]
[Folder 3] --> [Frame 4]

@enduml
```

</div>

[Learn More](https://sli.dev/guide/syntax.html#diagrams)


---
layout: center
class: text-center
---

# Learn More

[Documentations](https://sli.dev) · [GitHub](https://github.com/slidevjs/slidev) · [Showcases](https://sli.dev/showcases.html)
