<template>
  <div id="app">
    <h1>Sitio Subastas</h1>
    <VistaPrincipal msg="Subastas"/>
  </div>
</template>

<script>
import VistaPrincipal from './components/VistaPrincipal.vue'

export default {
  name: 'App',
  components: {
    VistaPrincipal
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
