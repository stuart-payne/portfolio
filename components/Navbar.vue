<template>
  <div class="nav">
    <nuxt-link class="item" to="/">Home</nuxt-link>
    <nuxt-link class="item" to="/portfolio">Portfolio</nuxt-link>
    <a class="item" href="">Github</a>
  </div>
</template>

<style scoped>
.nav {
  display: flex;
  flex-direction: row;
  justify-content: center;
  border-bottom: 1px solid hsla(219, 100%, 4%, 1);
}

.item {
  height: 1.5em;
  padding: 1.5em;
  text-decoration: none;
  color: hsla(219, 100%, 4%, 1);
}

.item:visited,
.item:link,
.item:active {
  text-decoration: none;
  color: #000000;
}

.item:hover {
  color: white;
  background: hsla(219, 100%, 4%, 1);
}
</style>
