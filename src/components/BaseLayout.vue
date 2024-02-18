<script setup lang="ts">
import Sidebar from './bars/Sidebar.vue';
import Topbar from './bars/Topbar.vue';
</script>

<template>
  <div class="container">
    <div class="sidebar-container">
      <Sidebar />
    </div>
    <nav class="topbar-container">
      <Topbar />
    </nav>
    <main class="main">
      <slot> </slot>
    </main>
  </div>
</template>
  
<style>
.container {
  width: 100%;
  max-width: 1440px;
  min-height: 100vh;
  display: grid;
  grid-template-columns: 94px auto;
  grid-template-rows: 64px auto;
  gap: 0px 0px;
  grid-auto-flow: row;
  background-color: #060B13;
  grid-template-areas:
    "sidebar-container topbar-container"
    "sidebar-container main";
}

.sidebar-container {
  grid-area: sidebar-container;
  border-right: 1px var(--black-tertiary) solid;
}

.topbar-container {
  grid-area: topbar-container;
  border-bottom: 1px var(--black-tertiary) solid;
}

.main {
  grid-area: main;
  height: 100%;
  display: flex;
  flex-direction: column;
}
</style>