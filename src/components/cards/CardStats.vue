<script setup lang="ts">
import IconTrend from '../icons/IconTrend.vue'
import { defineProps } from 'vue'

interface IProps {
    value: string
    percentage: string
    label: string
    badgeColor: "red" | "green",
    showChart: boolean
}
const props = defineProps<IProps>()
</script>

<template>
    <div :class="['stats-card', {
        'green-chart': showChart,
    }]">
        <span class="value">
            {{ value }}
        </span>
        <span :class="['badge', badgeColor]">
            <IconTrend /> {{ percentage }}%
        </span>
        <span class="label">
            {{ label }}
        </span>
    </div>
</template>

<style scoped>
.stats-card {
    background-color: rgba(6, 11, 19, 0.32);
    min-width: 12.375rem;
    border-right: var(--black-tertiary) 1px solid;
    display: grid;
    grid-template-rows: 1fr 1fr;
    grid-template-columns: 1fr 1fr;
    padding: 0.75rem 1rem;
    align-content: space-between;
    justify-content: space-between;
    height: 68px;
}

.stats-card .value {
    font-size: 1.125rem;
    color: white;
    font-weight: 500;
}

.stats-card .label {
    white-space: nowrap;
    font-size: 0.75rem;
    color: rgba(255, 255, 255, 0.2);
    font-weight: 400;
}

.stats-card.green-chart {
    background-image: url(/green-chart.svg);
    background-repeat: no-repeat;
    background-position: right bottom;
}

.badge {
    padding: 1px 0.25rem;
    border-radius: 1.875rem;
    color: black;
    font-size: 0.75rem;
    font-weight: 500;
    display: flex;
    align-items: center;
    justify-content: center;
    width: fit-content;
    height: fit-content;
    line-height: 1rem;
    justify-self: flex-end;
}

.badge.green {
    background-color: #0CB47F;
}

.badge.red {
    background-color: #F37361;
}
</style>