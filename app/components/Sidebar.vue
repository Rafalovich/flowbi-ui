<template>
  <aside class="sidebar">
    <nav>
      <ul>
        <li v-for="item in menu" :key="item.to">
          <NuxtLink :to="item.to">{{ item.label }}</NuxtLink>
        </li>
      </ul>
    </nav>
  </aside>
</template>

<script setup>
const props = defineProps({
  menu: {
    type: Array,
    required: true,
    default: () => [],
  },
})
</script>

<style scoped>
.sidebar {
  width: 250px;
  height: 100vh;
  background-color: #f4f4f4;
  padding: 1rem;
  position: fixed;
  left: 0;
  top: 0;
}
nav ul {
  list-style: none;
  
}
nav li {
  margin: 1rem 0;
}
a {
  text-decoration: none;
  color: #333;
}
</style>
