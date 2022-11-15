<template>
  <div id="app">
    <contenu>

    </contenu>
  </div>
</template>


<script>

import ContenuModale from './components/ContenueModale.vue'

export default {
  name: 'App',
  components: {
    'contenu': ContenuModale
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
