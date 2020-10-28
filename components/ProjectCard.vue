<template>
  <div class="card" @click="() => (window.location.href = link)">
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
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-decoration: none;
  padding: 10px;
}

.card:hover {
  background-color: rgb(218, 218, 218);
}

.description {
  min-height: 50px;
  margin: 20px 10px;
}

.tags {
  display: flex;
}

.tag {
  margin: 4px;
  padding: 6px;
  border: 1px solid black;
  border-radius: 12px;
}

.title {
  font-size: 24px;
}
</style>
