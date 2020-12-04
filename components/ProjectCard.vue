<template>
  <a class="card" :href="link">
    <h2 class="title">{{ title }}</h2>
    <p class="description">{{ description }}</p>
    <div class="tags">
      <!-- tag logic here -->
      <div v-for="tag in tags" :key="tag" class="tag">{{ tag }}</div>
    </div>
  </a>
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
  color: white;
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-decoration: none;
  padding: 4px;
  border: 4px solid #1a2b46;
  transition: border 0.5s;
}

a:hover,
a:visited,
a:link,
a:active {
  text-decoration: none;
}

.card:hover {
  border: 4px solid white;
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
  font-style: italic;
  padding: 6px;
  border-bottom: 1px solid #35495e;
  border-radius: 8px;
}

.title {
  font-size: 24px;
}
</style>
