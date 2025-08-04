<!-- <template>
  <div>
<<<<<<< HEAD:app.vue
    <NuxtRouteAnnouncer />
    
    <NuxtWelcome />
=======
    <Sidebar :menu="MenuItems" />
    <NuxtPage />
>>>>>>> fbc70e779e7c0556518eb74757a2ae17740b41ad:app/app.vue
  </div>
</template> -->
<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
<script setup>
const MenuItems = useMenuItems()
</script>

