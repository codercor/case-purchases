<script lang="ts" setup>
import { defineProps } from 'vue';
export interface IProps {
    data: [
        {
            content: string;
            style: "shy" | "brash"
        }
    ],
    isDark: boolean
}
defineProps<IProps>();
</script>

<template>
    <tr :class="isDark ? 'dark' : 'light'">
        <td v-for="item in data" :class="item.style" :key="item.content"> {{ item.content }} </td>
    </tr>
</template>

<style scoped>
.light {
    background-color: #151921;
}

.dark {
    background-color: #0d121a
}

tr {
    display: flex;
    width: 100%;
    height: 58px;
}
td{
    flex: 1 1 auto;
    display: flex;
    justify-content: start;
    align-items: center;
    color: white;
    text-align: left;
    font-size:  0.875rem;;
    font-weight: 400;
    border-bottom: 1px solid #1E1E1E;
}
.shy{
    font-size: 0.775rem;
    color: #88888A;
}
</style>