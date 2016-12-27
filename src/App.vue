<template>
  <div id="app">
    <navigation></navigation>
    <div class="container-fluid">
      <ratings></ratings>
    </div>
  </div>
</template>

<script>
import Navigation from './components/Navigation'
import Ratings from './components/Ratings'

export default {
  name: 'app',
  components: {
    Navigation, Ratings
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
