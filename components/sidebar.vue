<template>
    <aside class="sidebar">
       <h2 class="title">תפריט</h2>
       <SidebarItem v-for="item in items" :key="item.title" :item="item" />
    </aside>
</template>

<script setup lang="ts">
import SidebarItem from './sidebarItem.vue';

const items = [
  { title: 'ראשי', icon: '🏠', link: '/' },
  { title: 'משתמשים', icon: '👥', children: [
    { title: 'רשימה', link: '/users' },
    { title: 'חדש', link: '/users/new' }
  ]},
  { title: 'הגדרות', icon: '⚙️', link: '/settings' }
]
</script>

<style scoped>
.sidebar {
    width: 250px;
    background-color: #f8f4f4;
    color: black;
    padding: 1rem;
}
.title {
    font-size: 1.4rem;
    margin-bottom: 1rem;
}
</style>