<template>
  <div>
    <div class="pills" v-for="dataSales in dataPill" :key="dataSales.id">
      <h6 class="pills-title">
        {{ dataSales.title }}
      </h6>
      <div class="pills-card" v-bind:class="{ bgprimary: type == 'primary', bgsecondary: type == 'secondary', bgviolet: type == 'violet' }">
        {{ dataSales.amount }}
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["dataPill", "type"]
};
</script>
<style lang="scss" scoped>
.pills-title {
  color: #444;
  font-size: 0.7em;
  margin-bottom: 5px;
}
.pills-card {
//   background: gray;
  font-size: 0.8em;
  padding: 5px 7px;
  color: white;
  font-weight: 600;
  border-radius: 4px;
}

.bgprimary {
    background: #7B9EF4;
}
.bgsecondary {
    background: #5ACFBC;
}
.bgviolet {
    background: #BA80E2;
}
</style>
