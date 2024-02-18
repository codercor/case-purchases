<script setup lang="ts">
import BaseLayout from './components/BaseLayout.vue';
import Stats from './components/Stats.vue';
import OrdersTable from './components/tables/OrdersTable.vue';
</script>

<template>
  <BaseLayout>
    <Stats />
    <OrdersTable />
  </BaseLayout>
</template>

<style scoped></style>
