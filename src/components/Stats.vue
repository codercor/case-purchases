<script setup lang="ts">
import CardStats from './cards/CardStats.vue'
</script>
<template>
    <div class="stats">
        <div class="date-select">
            <select name="date" id="date">
                <option value="today">Today</option>
            </select>
        </div>
        <CardStats value="432" percentage="55.9" label="Orders" badgeColor="green" :showChart="true" />
        <CardStats value="1389" percentage="20.9" label="Ordered items" badgeColor="green" :showChart="false" />
        <CardStats value="12" percentage="55.9" label="Returned items" badgeColor="green" :showChart="false" />
        <CardStats value="$43,245.68" percentage="55.9" label="Total Revenue" badgeColor="green" :showChart="true" />
        <CardStats value="$189.67" percentage="20.9" label="Average Revenue" badgeColor="red" :showChart="false" />
        <CardStats value="12h 12m" percentage="10" label="Time to fulfill" badgeColor="green" :showChart="false" />
    </div>
</template>

<style scoped>
.stats {
    display: grid;
    grid-template-columns: 9.875rem repeat(6, 1fr);
    border-bottom: var(--black-tertiary) 1px solid;
    height: 68px;
    width: 100%;
}  

.date-select {
    display: flex;
    align-items: center;
    justify-content: center;
    border-right: var(--black-tertiary) 1px solid;
}

.date-select select {
    width: fit-content;
    height: 100%;
    border: none;
    background-color: transparent;
    color: var(--white-primary);
    font-size: 1rem;
    text-align: center;
    cursor: pointer;
    outline: none;
}

.date-select select option {
    background-color: var(--black-secondary);
    color: var(--white-primary);
    font-size: 1rem;
    text-align: center;
}

.date-select select option:hover {
    box-shadow: 0 0 10px 100px #cfd2d3 inset;
}
</style>