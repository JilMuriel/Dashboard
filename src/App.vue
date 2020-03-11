<template>
  <div id="app">
    <Navbar />
    <CardGroup />
    <Statistics />
    <Performance />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import CardGroup from "./components/CardGroup";
import Statistics from "./components/Statistics.vue";
import Performance from "./components/Performance.vue";
export default {
  name: "App",
  components: {
    Navbar,
    CardGroup,
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
  font-size: 16px;
  font-family: "Poppins", sans-serif;
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
  background: #f4f5f9;
  height: 100%;
}
</style>
