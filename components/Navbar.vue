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
  border-bottom: 1px solid hsla(219, 100%, 4%, 1);
}

.item {
  font-size: 1.2em;
  height: 1.5em;
  padding: 1.5em;
  text-decoration: none;
  color: #35495e;
  transition: background-color 0.5s;
  transition: color 0.5s;
}

.item:visited,
.item:link,
.item:active {
  text-decoration: none;
  color: #35495e;
}

.item:hover {
  color: white;
  background-color: #35495e;
}
</style>
