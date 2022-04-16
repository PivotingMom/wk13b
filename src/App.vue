<template>
  <div id="app">
    <DataLayout />
  </div>
</template>

<script>
import DataLayout from './components/DataLayout.vue'

export default {
  name: 'App',
  components: {
    DataLayout
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
  margin-top: 60px;
}
</style>
