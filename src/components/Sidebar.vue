<script setup lang="ts">
import IconContentModel from './icons/IconContentModel.vue';
import IconExperiments from './icons/IconExperiments.vue';
import IconFunnels from './icons/IconFunnels.vue';
import IconHelp from './icons/IconHelp.vue';
import IconHome from './icons/IconHome.vue';
import IconLogo from './icons/IconLogo.vue';
import IconPurchases from './icons/IconPurchases.vue';
import IconSettings from './icons/IconSettings.vue';
import IconLogout from './icons/IconLogout.vue';

</script>
<template>
    <div class="content">
        <IconLogo />
        <nav>
            <ul>
                <IconHome />
                <IconFunnels />
                <IconContentModel />
                <IconPurchases />
                <IconExperiments />
                <IconSettings />
            </ul>
        </nav>
        <div class="actions">
            <IconHelp />
            <IconLogout />
        </div>
    </div>
</template>

<style scoped>
.content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    padding-top: 18px;
    gap:107px;
}

 

ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

.actions {
    display: flex;
    flex-direction: column;
}
</style>