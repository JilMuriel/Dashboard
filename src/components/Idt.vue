<template>
  <div>
    <div class="ind-item" v-for="dataProp in propsData" :key="dataProp.id">
      <div class="ind-box" v-bind:class="{ bgprimary: type == 'primary', bgsecondary: type == 'secondary', bgviolet: type == 'violet' }"></div>
      <span class="ind-title">{{ dataProp.title }}</span>
    </div>
  </div>
</template>
<script>
export default {
  props: ["propsData", "type"]
};
</script>
<style lang="scss">
.ind-item {
  display: flex;
  align-items: center;
  margin-right: 8px;
}
.ind-box {
  height: 10px;
  width: 10px;
  margin-right: 4px;
}
.ind-title {
  font-size: 0.7em;
  font-weight: 600;
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
