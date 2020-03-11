<template>
  <div class="card-container">
    <div
      class="card"
      v-for="item in salesData"
      :key="item.id"
    >
      <div class="card-head">
        <h3 class="card-head__title">Sales</h3>
        <img src="@/assets/img/info-icon.png" />
      </div>
      <div class="card-body">
        <div class="card-content__left">
          <div class="pill pill-primary">
            <span>20%</span>
            <img src="@/assets/img/arrow-icon.png" />
          </div>
        </div>
        <div class="card-content__right">
          <div class="sales-content">
            <p class="text-secondary">Lifetime Sales</p>
            <section class="sales">
              <img src="@/assets/img/ph-icon.png" />
              <span>175,000</span>
            </section>
          </div>
          <div class="sales-content">
            <p class="text-secondary">Revenue Sales</p>
            <section class="sales">
              <img src="@/assets/img/ph-icon.png" />
              <span>170,000</span>
            </section>
          </div>
        </div>
      </div>
      <div class="card-footer">
        <div class="card-footer__container" style="padding: 13px 20px">
          <p><small>Average Order Value</small></p>
          <small class=" ml-auto">
            <section class="sales">
              <img src="@/assets/img/ph-icon.png" />
              <span>170,000</span>
            </section>
          </small>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["salesData"]
};
</script>
<style lang="scss" scoped>
.card-container {
  padding: 40px;
  max-width: 1500px;
  margin: auto;
  display: grid;
  grid-gap: 20px;
  grid-template-columns: repeat(4, 1fr);
  border: 1px solid black;
  @media only screen and (max-width: 900px) {
    grid-template-columns: repeat(2, 1fr);
  }
  @media only screen and (max-width: 426px) {
    grid-template-columns: 1fr;
  }
}
.card {
  background: white;
  position: relative;
  border-radius: 4px;
  box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.13);
}
.card-head {
  padding: 15px 20px 10px;
  display: flex;
  align-items: center;
  img {
    cursor: pointer;
    max-width: 15px;
  }
}
.card-body {
  padding: 0px 20px 70px;
  display: grid;
  align-items: center;
  grid-template-columns: auto 1fr;
  .card-content__left {
    text-align: left;
  }
  .card-content__right {
    text-align: right;
    margin-left: auto;
  }
}
.card-footer {
  margin-top: auto;
  position: absolute;
  width: 100%;
  bottom: 0;
  border-top: 1.2px solid rgb(214, 214, 214);
  .card-footer__container {
    display: flex;
  }
}

.card-head__title {
  font-weight: normal;
  margin-right: 8px;
  font-size: 1.1em;
}

.pill {
  height: 30px;
  font-size: 13px;
  color: rgba(0, 0, 0, 0.6);
  line-height: 32px;
  padding: 0 14px;
  border-radius: 16px;
  background-color: #e4e4e4;
  margin-right: 5px;
  span {
    margin-right: 9px;
  }
  img {
    max-width: 10px;
  }
}
.pill-primary {
  background: #7d9ffc;
  color: #fff;
}
.sales {
  img {
    margin-right: 5px;
    position: relative;
    top: 2px;
    max-height: 14px;
  }
  span {
    font-weight: bold;
    font-size: 1.1em;
  }
}
.text-secondary {
  color: #808080;
  font-size: 0.7em;
  max-width: 85px;
  margin-bottom: 5px;
}
.sales-content {
  margin-top: 10px;
}
.ml-auto {
  margin-left: auto;
}
small {
  color: #808080;
  font-size: 0.7em;
  font-weight: normal;
}
</style>
