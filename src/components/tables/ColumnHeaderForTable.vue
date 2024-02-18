<script setup lang="ts">
import { defineProps, type Component } from 'vue';
import { IconArrowSort } from '../icons';
interface IProps {
    header: {
        name: string;
        key: string;
        icon: Component,
        sortable: boolean
    },
}
defineProps<IProps>();
</script>
<template>
    <th>
        <header.icon /> <span>{{ header.name }}</span>

        <div class="sort" v-if="header.sortable">
            <span>
                <IconArrowSort :selected="true" />
            </span>
            <span>
                <IconArrowSort :selected="false" />
            </span>
        </div>
    </th>
</template>

<style scoped>
th {
    display: flex;
    align-items: center;
    line-height: 100%;
    gap: 0.25rem;
}

.sort {
    margin-left: auto;
    display: flex;
    cursor: pointer;
    flex-direction: column;
}

.sort span:nth-child(2){
    rotate: 180deg;
}
</style>

