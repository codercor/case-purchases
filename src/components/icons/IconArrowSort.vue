<script setup lang="ts">

import { defineProps } from 'vue';

interface IProps{
    selected: boolean;
}

defineProps<IProps>();
</script>

<template>
    <svg width="8" height="5" viewBox="0 0 8 5" fill="none" xmlns="http://www.w3.org/2000/svg">
        <g clip-path="url(#clip0_1_1209)">
            <path d="M1 3.78574L4 0.785736L7 3.78574" :stroke="selected ? '#fff':'#88888A' " stroke-width="0.857143" stroke-linecap="round"
                stroke-linejoin="round" />
            <path d="M1 3.78574L4 0.785736L7 3.78574" stroke="black" stroke-opacity="0.2" stroke-width="0.857143"
                stroke-linecap="round" stroke-linejoin="round" />
        </g>
        <defs>
            <clipPath id="clip0_1_1209">
                <rect width="8" height="5" fill="white" />
            </clipPath>
        </defs>
    </svg>
</template>