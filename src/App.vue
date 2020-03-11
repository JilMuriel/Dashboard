<template>
  <div id="app">
    <Navbar />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Navbar
  }
}
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css?family=Poppins&display=swap');
  html {
    font-size: 16px;
    font-family: 'Poppins', sans-serif;
  }
  * {
    margin: 0px;
  }
  body {
    box-sizing: border-box;
    margin: 0;
  }
</style>
