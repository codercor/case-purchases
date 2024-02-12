<template>
  <div class="container">
    <div class="sidebar"></div>
    <nav class="topbar"></nav>
    <main class="main"></main>
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
  grid-template-areas:
    "sidebar topbar"
    "sidebar main";
}

.sidebar {
  grid-area: sidebar;
  background-color: #060B13;
  border-right: 1px #212830 solid;
}

.topbar {
  grid-area: topbar;
  background-color: #060B13;
  border-bottom: 1px #212830 solid;
}

.main {
  grid-area: main;
  background-color: #1E1E1E;
}
</style>