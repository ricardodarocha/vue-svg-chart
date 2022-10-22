<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Grafico w=600 h=400 color="#f0b305" />
  </div>
</template>

<script>
import Grafico from './components/Grafico.vue'

export default {
  name: 'App',
  components: {
    Grafico
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
