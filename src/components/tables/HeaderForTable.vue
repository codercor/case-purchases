<script setup lang="ts">
import { defineProps } from 'vue';
import FilterInputForTable from './FilterInputForTable.vue';
import SearchInputVue from '../inputs/SearchInput.vue';
interface IProps {
    title: string;
    subtitle?: string;
}
defineProps<IProps>();
</script>

<template>
    <div class="table-header">
        <div class="title">
            <h3> {{ title }} </h3>
            <p v-if="subtitle"> {{ subtitle }} </p>
        </div>
        <div class="actions">
            <FilterInputForTable/>
            <SearchInputVue/>
        </div>
    </div>
</template>

<style scoped>
.table-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: white;
    margin-bottom: 1rem;
}

.title{
    display: flex;
    gap:0.5rem;
    align-items: center;
}

.table-header .title h3 {
    font-size: 1.375rem;
    font-weight: 500;
}

.table-header .title p {
    font-size: 1.125rem;
    font-weight: 400;
    color: #88888A;
}

.actions{
    height: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
}
</style>