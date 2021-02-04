<template>
  <div>
    <Navbar />
    <div class="content">
      <div class="leftContent"></div>
      <div class="mainContent">
        <Nuxt />
      </div>
      <div class="rightContent"></div>
    </div>
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
  background: linear-gradient(#234a88, #a63e3e);
  min-height: 100vh;
}
.content {
  display: grid;
  grid-template-columns: 1fr minmax(0, 600px) 1fr;
  grid-auto-rows: minmax(100px, auto);
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
  margin: 0;
}
</style>
