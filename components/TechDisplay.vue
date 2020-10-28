<template>
  <div class="container">
    <div class="head">{{ experience }}</div>
    <div v-for="tech in techs" :key="tech" class="tech">{{ tech }}</div>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    experience: {
      type: String,
      required: true,
    },
    techs: {
      type: Array,
      required: true,
    },
  },
})
</script>
<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.head {
  text-align: center;
  font-weight: bold;
  font-size: 1em;
  border-bottom: 1px solid black;
}

.tech {
  font-size: 0.8em;
}
</style>
