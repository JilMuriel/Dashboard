<template>
  <div class="container">
    <h1>{{ title }}</h1>
    <div class="container-header">
        <button>asdasd</button>
        <button>asdasd</button>
    </div>
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
  .container-header {
      display: flex;
      flex-direction: row;
  }
}
</style>
