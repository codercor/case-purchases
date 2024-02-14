<script setup lang="ts">
import SearchInput from '../inputs/SearchInput.vue';
import AiAvatar from '../../assets/ai-avatar.png'
import IconNotifyVue from '../icons/IconNotify.vue';
</script>

<template>
    <div class="topbar">
        <SearchInput />
        <div class="actions">
            <img :src="AiAvatar" alt="Start ai assistant" />
            <IconNotifyVue />
        </div>
        <div class="profile-button">
            <div class="user-avatar">
                <span>U</span>
            </div>
            <span>User name</span>
        </div>
    </div>
</template>

<style scoped>
.topbar {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    padding: 0 1rem;
    background-color: #060B13;
    height: 100%;
    gap: 2rem;
}

.actions {
    display: flex;
    gap: 1.5rem;
}

.profile-button {
    display: flex;
    gap: 0.5rem;
    align-items: center;
    cursor: pointer;
    border-radius: 0.5rem;
    border: 1px solid var(--black-tertiary);
    background-color: #0D121A;
    height: 2.5rem;
    width: 8.375rem;
    padding: 0.25rem;
}
.profile-button .user-avatar {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #AA96F3;
    border-radius: 2rem;
    line-height: 100%;
    height: 2rem;
    width: 2rem;
    font-size: 1rem;
    font-weight: 400;
}

.profile-button span {
    font-size: 0.875rem;
    font-weight: 400;
    color: var(--white-primary);
}

</style>