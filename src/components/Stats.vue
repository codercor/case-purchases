<template>
    <div class="stats">
        <div class="stats-card date-select"></div>
        <div class="stats-card"></div>
        <div class="stats-card"></div>
        <div class="stats-card"></div>
        <div class="stats-card"></div>
        <div class="stats-card"></div>
        <div class="stats-card"></div>
    </div>
</template>

<style scoped>
.stats {
    display: grid;
    grid-template-columns: 9.875rem repeat(6, 1fr);
    height: 68px;
    width: 100%;
}
.stats-card {
    background-color: rgba(6, 11, 19, 0.32);
    border-bottom: #212830 1px solid;
    border-right: #212830 1px solid;
}
.stats-card:not(:first-child) {
    min-width: 12.375rem;
}
</style>