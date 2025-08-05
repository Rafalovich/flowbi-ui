<template>
    <div class="layout rtl">
        <navbar/>
        <sidbar/>
        
        <div class="content">
           <NuxtPage />
        </div>
    </div>
</template>

<script setup>
import Navbar from '../components/Navbar.vue';
import Sidbar from '../components/Sidebar.vue'

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