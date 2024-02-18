<script lang="ts" setup>
import {
    IconDate,
    IconUser,
    IconTotal,
    IconFile,IconEmail,IconPrimaryProduct
} from '../icons'
import ColumnHeaderForTable from './ColumnHeaderForTable.vue';
import HeaderForTable from './HeaderForTable.vue';
import RowForTableVue, { type IProps as IPropsRowForTable } from './RowForTable.vue';
import { ref, computed, type ComputedRef } from 'vue';
const mockData = {
    headers: [
        { name: "Date", key: "date", icon: IconDate, sortable: true },
        { name: "Order ID", key: "orderId", icon: IconFile, sortable: false },
        { name: "Customer Name", key: "customerName", icon: IconUser, sortable: false },
        { name: "Email Address", key: "email", icon: IconEmail, sortable: false },
        { name: "Primary Product", key: "primaryProduct", icon: IconPrimaryProduct, sortable: false },
        { name: "Total Payment", key: "totalPayment", icon: IconTotal, sortable: false }
    ],
    orders: [
        {
            date: "30 Jan, 2023 at 4:23 AM",
            orderId: "123456",
            customerName: "John Doe",
            email: "x.com",
            primaryProduct: "Product 1",
            totalPayment: "$100"
        },
        {
            date: "30 Jan, 2023 at 4:23 AM",
            orderId: "123456",
            customerName: "John Doe",
            email: "x.com",
            primaryProduct: "Product 1",
            totalPayment: "$100"
        },
        {
            date: "30 Jan, 2023 at 4:23 AM",
            orderId: "123456",
            customerName: "John Doe",
            email: "x.com",
            primaryProduct: "Product 1",
            totalPayment: "$100"
        },
        {
            date: "30 Jan, 2023 at 4:23 AM",
            orderId: "123456",
            customerName: "John Doe",
            email: "x.com",
            primaryProduct: "Product 1",
            totalPayment: "$100"
        },
        {
            date: "30 Jan, 2023 at 4:23 AM",
            orderId: "123456",
            customerName: "John Doe",
            email: "x.com",
            primaryProduct: "Product 1",
            totalPayment: "$100"
        },
        {
            date: "30 Jan, 2023 at 4:23 AM",
            orderId: "123456",
            customerName: "John Doe",
            email: "x.com",
            primaryProduct: "Product 1",
            totalPayment: "$100"
        },
        {
            date: "30 Jan, 2023 at 4:23 AM",
            orderId: "123456",
            customerName: "John Doe",
            email: "x.com",
            primaryProduct: "Product 1",
            totalPayment: "$100"
        },
        {
            date: "30 Jan, 2023 at 4:23 AM",
            orderId: "123456",
            customerName: "John Doe",
            email: "x.com",
            primaryProduct: "Product 1",
            totalPayment: "$100"
        },
        {
            date: "30 Jan, 2023 at 4:23 AM",
            orderId: "123456",
            customerName: "John Doe",
            email: "x.com",
            primaryProduct: "Product 1",
            totalPayment: "$100"
        },
        {
            date: "30 Jan, 2023 at 4:23 AM",
            orderId: "123456",
            customerName: "John Doe",
            email: "x.com",
            primaryProduct: "Product 1",
            totalPayment: "$100"
        }
    ]
}

const headers = ref(mockData.headers);
const orders = ref(mockData.orders);

const rows = computed(() => {
    return orders.value.map((order, index) => {
        const rowData = Object.values(order)
            .map((value, index) => {
                return {
                    content: value,
                    style: index === 0 ? "shy" : "brash"
                }
            })
        return {
            data: rowData,
            isDark: index % 2 === 0
        }
    })
}) as ComputedRef<IPropsRowForTable[]>;

</script>
<template>
    <div class="table-container">
        <HeaderForTable title="Orders" subtitle="(10 out of 286)" />
        <table>
            <thead>
                <tr>
                    <ColumnHeaderForTable v-for="(header, index) in headers" :key="index" :header="header" />
                </tr>
            </thead>
            <tbody>
                <RowForTableVue v-for="(order, index) in rows" :key="index" :data="order.data" :isDark="index % 2 === 0" />
            </tbody>
        </table>
    </div>
</template>

<style>
.table-container {
    padding: 2rem;
    width: 100%;
    display: flex;
    flex-direction: column;
    flex: 0.9 1 auto;
}

table {
    width: 100%;
    color: #88888A;
    background-color: #0D121A;
    border: 1px solid hsl(0, 0%, 12%);
    overflow: hidden;
    height: fit-content;
    border-radius: 0.5rem;
}

table thead tr {
    display: flex;
    width: 100%;
    height: 42px;
    align-items: center;
}

/* padding: 1rem 1.5rem;
 */


table th,
table td {
    flex: 1 1 auto;
    width: 100%;
    text-align: left;
    padding: 0rem 1.5rem;
    border-bottom: 1px solid #1E1E1E;
    border-right: 1px solid #1E1E1E;
    font-size: 0.775rem;
    color: #88888A;
    height: 100%;
    display: flex;
    align-items: center;
}

table th+table td:last-child {
    border-right: none;
}
</style>