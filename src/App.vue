<template>
  <div id="app">
    <HomeMeme msg="UltiMEME GENERATOR"/>
  </div>
</template>

<script>
import HomeMeme from './components/HomeMeme.vue'

export default {
  name: 'App',
  components: {
    HomeMeme
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
