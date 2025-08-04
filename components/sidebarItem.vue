<template>
    <div>
        <div class="item" @click="toggle">
            <span class="icon">{{ item.icon }}</span>
            <NuxtLink v-if="item.link" :to="item.link" class="link">{{ item.title }}</NuxtLink>
            <span v-else class="title">{{ item.title }}</span>
        </div>
        <div v-if="item.children && open" class="children">
            <NuxtLink v-for="child in item.children" :key="child.title" :to="child.link" class="child-link">
                {{ child.title }}
            </NuxtLink>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
interface MenuItem {
  icon: string;
  title: string;
  link?: string;
  children?: { title: string; link: string }[];
}
const props = defineProps<{item: MenuItem}>(); 
const open = ref(false);

function toggle() {
  if (props.item.children) {
    open.value = !open.value
  }
}
</script>

<style scoped lang="scss">
.item {
  padding: 0.5rem 0;
  cursor: pointer;
  display: flex;
  align-items: center;
}
.icon {
  margin-left: 0.5rem;
}
.link {
  color: rgb(214, 22, 22);
  text-decoration: none;
}
.children {
  margin-right: 1rem;
}
.child-link {
  display: block;
  color: #0db7e1;
  margin: 0.3rem 0;
  text-decoration: none;
  padding-right: 1rem;
}
.child-link:hover {
  color: #1abc9c;
}
</style>
       
