<template>
  <div class="nav">
    <nuxt-link class="item" to="/">Home</nuxt-link>
    <nuxt-link class="item" to="/portfolio">Portfolio</nuxt-link>
    <a class="item" href="https://github.com/stuart-payne">Github</a>
  </div>
</template>

<script>
import Vue from 'vue'
export default Vue.extend({})
</script>

<style scoped>
.nav {
  display: flex;
  flex-direction: row;
  justify-content: center;
  border-bottom: 2px solid white;
}

.item {
  font-size: 1.1em;
  height: 1.5em;
  padding: 1.5em;
  border-bottom: 4px solid #1a2b46;
  margin-bottom: 1px;
  text-decoration: none;
  transition: border-bottom 0.5s;
}

.item:visited,
.item:link,
.item:active {
  text-decoration: none;
  color: white;
}

.item:hover {
  border-bottom: 4px solid white;
}
</style>
