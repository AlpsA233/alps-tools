<script setup lang="ts">
import { ref } from 'vue';

const categories = ref([
  { id: 1, name: '文本处理' },
  { id: 2, name: '图像编辑' },
  // ... more categories
]);

const featuredTools = ref([
  { id: 1, name: 'Featured Tool 1' },
  { id: 2, name: 'Featured Tool 2' },
  // ... more tools
]);

</script>

<template>
  <main class="main-content">
    <section class="tool-categories">
      <div v-for="category in categories" :key="category.id" class="category-card">
        {{ category.name }}
      </div>
    </section>
    <section class="featured-tools">
      <div v-for="tool in featuredTools" :key="tool.id" class="tool-card">
        {{ tool.name }}
      </div>
    </section>
  </main>
</template>

<style scoped>
.main-content {
  display: flex;
  justify-content: space-between;
  padding: 1em;
}
.tool-categories, .featured-tools {
  width: 48%;  /* Adjust as needed */
}
.category-card, .tool-card {
  padding: 1em;
  margin: 0.5em;
  background-color: #e6e6e6;
}
</style>