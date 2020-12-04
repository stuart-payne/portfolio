<template>
  <div class="content">
    <div class="leftContent"></div>
    <div class="mainContent">
      <Navbar />
      <Nuxt />
    </div>
    <div class="rightContent"></div>
  </div>
</template>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background-color: #1a2b46;
}
.content {
  display: grid;
  grid-template-columns: 1fr minmax(0, 800px) 1fr;
  grid-auto-rows: minmax(100px, auto);
  min-height: 100vh;
}

.leftContent {
  grid-column: 1;
  /* background-color: hsl(0, 90%, 90%); */
}

.rightContent {
  grid-column: 3;
  /* background-color: hsl(120, 90%, 90%); */
}

.mainContent {
  grid-column: 2;
  /* background-color: hsl(240, 90%, 90%); */
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
