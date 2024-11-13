---
theme: default
title: The React.js way
class: text-left

layout: statement
transition: fade
---

## How does React.js solves those problems?

<div v-click class="mt-10">
  <p class="italic">"Uhhmm actually, it's not just React.js, but, modern tooling too!"</p>
</div>

---
theme: default
title: React.js in a nutshell
class: text-left

transition: fade
---

## React.js in a nutshell
___

<ul class="mt-10">
  <li v-click class="text-2xl">Allows you to build UI elements as reusable components</li>
</ul>
<br />
<img v-click src="/assets/ui-components.png" width="600" height="600" class="block mx-auto"/>

---
theme: default
title: React.js in a nutshell
class: text-left

transition: fade
---

## React.js in a nutshell
___

<ul class="mt-10">
  <li class="text-2xl">Handles synchronization of HTML Elements with Data (State)</li>
</ul>
<br />
<img v-click src="https://media.geeksforgeeks.org/wp-content/uploads/20231031094123/Peek-2023-10-31-09-40.gif" width="600" height="600" class="block mx-auto"/>

---
theme: default
title: React.js in a nutshell
class: text-left

transition: fade
---

## React.js + Modern tooling
___

<ul class="mt-10">
  <li class="text-2xl">Smooth JavaScript development experience (DX)</li>
</ul>
<br />

<div v-click class="flex items-center justify-around">
  <img src="https://flaviocopes.com/images/vite-react-app/Untitled%203.png" width="400" height="400" class="block"/>

  <img src="/assets/npm-install.png" width="450" height="450" class="block"/>
</div>

---
theme: default
title: Starting a new React.js project
class: text-left

transition: fade
---

## Starting a new React.js project 
___

<br />

<div  class="flex items-start justift-between">
  <div v-click class="flex-1">
    <div>System requirements: </div>
    <ul>
      <li class="text-blue-400 font-semibold">
        <a href="https://nodejs.org/en/download/package-manager" target="_blank">Node.js (for tooling)</a>
      </li>
        <li class="text-blue-400 font-semibold">
        <a href="https://nodejs.org/en/download/package-manager" target="_blank">Build tools (Vite, Webpack, Parcel, etc.)</a>
      </li>
    </ul>
  </div>

  <div v-click class="flex-1">
     <div>Build tools explained: </div>
      <ul>
        <li class="text-blue-400 font-semibold">
          <div>Vite: </div>
          <a href="https://vite.dev/guide/why" target="_blank">
            Why Vite?
          </a>
        </li>
        <br />
        <li class="text-blue-400 font-semibold">
          <div>Webpack: </div>
          <a href="https://peterxjang.com/blog/modern-javascript-explained-for-dinosaurs.html" target="_blank">
            Modern JavaScript Explained For Dinosaurs
          </a>
        </li>
      </ul>
  </div>
</div>

<v-click>
<div class="absolute -translate-y-5 flex gap-2 items-center">
  <span class="text-sm text-purple-400 italic">Build tool used in this example:</span>
  <img src="https://www.svgrepo.com/show/374167/vite.svg" width="30" height="30"  />
</div>

<span class="text-sm italic block -mb-2">Open your project's folder in your terminal</span>

-
  ```bash
  npm create vite@latest
  ```
</v-click>

<v-click>

<span class="text-sm italic block -mb-2">Install needed packages</span>

-
  ```bash
  npm install
  ```
</v-click>

<v-click>

<span class="text-sm italic block -mb-2">Run our app</span>

-
  ```bash
  npm run dev
  ```
</v-click>