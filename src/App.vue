<template>
  <div id="app">
    <Nav />
    <Projects />
  </div>
</template>

<script>
  import Nav from './components/Nav'
  import Projects from './components/Projects'

  export default {
    name: 'app',
    components: {
      Nav,
      Projects
    }
  }
</script>

<style>
  #app {
    font-family: 'CircularStd';
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #444;
  }
  img {
    max-width: 100%;
  }
</style>
