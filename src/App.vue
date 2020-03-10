<template>
  <div id="app">
    <Header />
    lorem
  </div>
</template>

<script>

import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style>
html, body {
    height: 100%;
    margin: 0px;
}
#app {
  height: 100%;
  background: #F4F5F9;
  position: absolute;
  width: 100%;
}
</style>
