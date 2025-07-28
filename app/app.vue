<template>
  <div>
    <Sidebar :menu="MenuItems" />
    <NuxtPage />
  </div>
</template>
<script setup>
const MenuItems = useMenuItems()
</script>

