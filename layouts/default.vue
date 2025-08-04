<template>
    <div class="layout rtl">
        <sidbar/>
        <div class="content">
           <NuxtPage />
        </div>
    </div>
</template>

<script setup>
import Sidbar from '~/components/sidebar.vue'
</script>

<style scoped>
.layout {
    display: flex;
    padding: 1rem;
    overflow-y: auto;
}
.rtl {
    direction: rtl;
}
</style>