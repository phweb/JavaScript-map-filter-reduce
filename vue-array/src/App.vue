<template>
  <div id="app">
    <Array msg="Manipulação de Arrays com map, filter, reduce, includes, find e foreach"/>
  </div>
</template>

<script>
import Array from './components/Array.vue'

export default {
  name: 'App',
  components: {
    Array
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0 auto;
}
#app img{
   margin: 0 auto;
}
</style>
