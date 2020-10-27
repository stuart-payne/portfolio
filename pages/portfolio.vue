<template>
  <div>
    <project-card
      v-for="project in projects"
      :key="project.title"
      :title="project.title"
      :description="project.description"
      :link="project.link"
      :tags="project.tags"
    ></project-card>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import ProjectCard from '../components/ProjectCard.vue'

export default Vue.extend({
  components: {
    ProjectCard,
  },
  data() {
    return {
      projects: require('../projects.json'),
    }
  },
})
</script>
