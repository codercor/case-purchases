<script setup lang="ts">
import IconSearch from '../icons/IconSearch.vue';
</script>
<template>
    <div class="input-container">
        <IconSearch />
        <input type="text" placeholder="Search">
    </div>
</template>

<style scoped>
.input-container {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.5rem 1rem;
    border-radius: 0.5rem;
    background-color: var(--black-tertiary);
    width:16.875rem;
    height: 2.5rem;
}
input{
    height:100%;
    flex: 1 1 auto;
    border: none;
    background-color: transparent;
    outline: none;
    color: #fff;
}
</style>