<template>
  <div id="app">
    <Hero />
    <Flavors />
    <Address />
  </div>
</template>

<script>
export default {
  name: 'App',
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  outline: none;
  box-sizing: border-box;
  font-family: 'Open Sans', sans-serif;
}

#app {
  width: 100%;
  min-height: 100vh;
}

html {
  scroll-behavior: smooth;
}

body {
  color: #f1f1f1;
}
</style>
