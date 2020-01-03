<template>
  <div id="app">
    <CesiumViewer></CesiumViewer>
  </div>
</template>

<script>
import CesiumViewer from './components/CesiumViewer.vue'

export default {
  name: 'app',
  components: {
    CesiumViewer
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 0;
  padding: 0;
  border: 0;
}
</style>
