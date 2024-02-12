<script setup lang="ts">
import Sidebar from './Sidebar.vue';
</script>
<template>
  <div class="container">
    <div class="sidebar">
      <Sidebar />
    </div>
    <nav class="topbar"></nav>
    <main class="main">
      <slot> </slot>
    </main>
  </div>
</template>
  
<style>
.container {
  width: 100%;
  max-width: 1440px;
  height: 100vh;
  display: grid;
  grid-template-columns: 94px auto;
  grid-template-rows: 64px auto;
  gap: 0px 0px;
  grid-auto-flow: row;
  background-color: #060B13;
  grid-template-areas:
    "sidebar topbar"
    "sidebar main";
}

.sidebar {
  grid-area: sidebar;
  border-right: 1px #212830 solid;
}

.topbar {
  grid-area: topbar;
  border-bottom: 1px #212830 solid;
}

.main {
  grid-area: main;
}
</style>