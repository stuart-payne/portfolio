<template>
  <div class="nav">
    <nuxt-link class="item" to="/">Home</nuxt-link>
    <nuxt-link class="item" to="/portfolio">Portfolio</nuxt-link>
    <a class="item" href="https://github.com/stuart-payne" target="_blank"
      >Github</a
    >
  </div>
</template>

<script>
import Vue from 'vue'
export default Vue.extend({})
</script>

<style scoped>
.nav {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  border-bottom: 1px solid white;
  background-image: linear-gradient(to right, #161616, #1c1c1c);
}

.item {
  font-size: 1.1em;
  padding: 0.8em 1.2em;
  border-top: 10px solid rgba(255, 255, 255, 0%);
  text-decoration: none;
  transition: border-top 0.5s;
}

.item:visited,
.item:link,
.item:active {
  text-decoration: none;
  color: white;
}

.item:hover {
  border-top: 10px solid rgba(255, 255, 255, 100%);
}
</style>
