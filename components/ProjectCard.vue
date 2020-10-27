<template>
  <div class="card">
    <h2 class="title">{{ title }}</h2>
    <p class="description">{{ description }}</p>
    <div class="tags">
      <!-- tag logic here -->
      <div v-for="tag in tags" :key="tag" class="tag">{{ tag }}</div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    tags: {
      type: Array,
      required: true,
    },
    link: {
      type: String,
      required: true,
    },
  },
})
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-decoration: none;
  border: 2px solid black;
  padding: 10px;
}

.description {
  min-height: 100px;
}

.tags {
  display: flex;
}

.tag {
  margin: 4px;
  padding: 4px;
  border: 2px solid black;
  border-radius: 6px;
}

.title {
  font-size: 24px;
}
</style>
