<template>
  <Locations />
</template>

<script>
import Locations from './components/Locations.vue'
export default {
  name: 'App',
  components: { Locations }
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

body {
  margin: 0;
  background-color: #d1d1e0;
}
</style>
