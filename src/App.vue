<template>
  <div id="app">
    <Hero />
    <Flavors />
  </div>
</template>

<script>
import Hero from './components/Hero'
import Flavors from './components/Flavors'

export default {
  name: 'App',
  components: {
    Hero,
    Flavors,
  },
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
