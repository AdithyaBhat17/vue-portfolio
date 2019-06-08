<template>
  <div id="app">
    <Nav />
  </div>
</template>

<script>
  import Nav from './components/Nav.vue'

  export default {
    name: 'app',
    components: {
      Nav
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
</style>
