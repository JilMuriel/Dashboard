<template>
  <div id="app">
    <Navbar />
    <Sales />
    <Statistics />
    <Performance />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Sales from "./components/Sales";
import Statistics from "./components/Statistics.vue";
import Performance from "./components/Performance.vue";
export default {
  name: "App",
  components: {
    Navbar,
    Sales,
    Statistics,
    Performance
  }
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Poppins&display=swap");
html,
body {
  height: 100%;
  margin: 0px;
}
html {
  font-size: 17px;
  font-family: "Open Sans", sans-serif;
}
* {
  margin: 0px;
}
body {
  box-sizing: border-box;
  margin: 0;
  height: 100%;
  background: #f4f5f9;
}
#app {

  height: 100%;
}
input {
    font-family: 'Open Sans', sans-serif;
    font-size: 0.9em!important;
}
select {
  font-size: 0.9em;
  margin-right: 13px;
  font-family: 'Open Sans', sans-serif;
}
</style>
