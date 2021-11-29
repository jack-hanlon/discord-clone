<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <frontend />
</template>

<script>
import frontend from './components/frontend.vue'
export default {
  name: 'App',
  components: {
    frontend
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
