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
  width: 200px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 0px 5px;
}

.head {
  text-align: center;
  font-weight: bold;
  font-size: 1.5em;
  border-bottom: 1px solid #35495e;
  padding-bottom: 4px;
  margin-bottom: 4px;
  width: 100%;
}

.tech {
  font-size: 1.2em;
  margin: 4px 0px;
}
</style>
