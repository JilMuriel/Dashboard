<template>
  <div class="container">
    <h1>{{ title }}</h1>
  </div>
</template>
<script>
export default {
  data: () => {
    return {
      title: "Hello from statistics"
    };
  }
};
</script>
<style lang="scss" scoped>
.container {
  padding: 40px;
  max-width: 1500px;
  margin: auto;
  border: 1px solid black;
}
</style>
