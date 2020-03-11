<template>
  <div id="app">
    <Navbar />
    <CardGroup/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import CardGroup from './components/CardGroup'

export default {
  name: 'App',
  components: {
    Navbar,
    CardGroup
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
    height: 100%;
  }
  #app {
    background: #F4F5F9;
    height: 100%;
  }
</style>
