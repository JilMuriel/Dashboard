<template>
  <div class="card">
    <div class="card-header">
      <p>
        <strong>{{ title }}</strong>
      </p>
      <img src="@/assets/img/info-icon.png" />
    </div>

    <div class="card-body">
      <div class="d-grid d-grid__head">
        <div>
          <h5 class="text-secondary">Branch</h5>
        </div>
        <div>
          <h5 class="text-secondary">Total Sales(<span><img class="currency-icon" src="@/assets/img/ph-icon.png" /></span>)</h5>
        </div>
      </div>
      <div class="d-grid" v-for="dataProp in dataProps" :key="dataProp.id">
        <div class="grid-item__left">
          <p>{{ dataProp.id }}</p>
          <p>{{ dataProp.branch }}</p>
        </div>
        <div class="grid-item__right">
          <p style="margin-left: 54px;">{{ dataProp.totalSales }}.00</p>
          <section class="percentage-section">
            <p class="text-right">{{ dataProp.percentage }}%</p>
            <img
              v-bind:class="{ rotate90: dataProp.increase == false }"
              src="@/assets/img/arrow-up-solid_green.png"
            />
          </section>
        </div>
      </div>
    </div>
    <div class="card-footer">
      asd

    </div>
  </div>
</template>
<script>
export default {
  props: ["title", "dataProps"]
};
</script>
<style lang="scss" scoped>
.card {
  background: #fff;
  border-radius: 3px;
  box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.13);
}
.card-header {
  display: flex;
  align-items: center;
  background: #f7f8fc;
  padding: 18px 25px;
  img {
    margin-left: 10px;
    margin-top: 3px;
  }
}
.card-footer {
  padding: 8px 20px;
  text-align: right;
}
.peso-icon {
  max-width: 10px;
  height: auto;
}
.d-grid {
  display: grid;
  grid-template-columns: 40% 1fr;
  padding: 10px 25px;
  border-bottom: 1.5px solid #f3f3f3;
}
.d-grid__head {
  padding-top: 14px;
  padding-bottom: 14px;
}
.grid-item__left {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-gap: 12px;
  p {
    font-size: 0.9em;
    color: #4d4d4d;
  }
}
.grid-item__right {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-gap: 12px;
}
.text-secondary {
  color: #b9b9b9;
  font-weight: 550;
  font-size: 1em;
}
.text-right {
  text-align: right;
}
p {
  font-family: "Open Sans", sans-serif;
  font-weight: 600;
}
.percentage-section {
  display: flex;
  align-items: center;
  margin-left: auto;
  img {
    margin-left: 7px;
    max-height: 14px;
    width: auto;
  }
}
.rotate90 {
  transform: rotate(180deg);
}
.rotate0 {
  transform: rotate(0deg);
}
.currency-icon {
    max-height: 13px;
    position: relative;
    left: 1px;
    margin: 0 2px;
}
</style>
