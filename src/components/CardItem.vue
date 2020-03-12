<template>
  <Fragment>
    <div class="card" v-for="prop in propss" :key="prop.id" tabindex="1">
      <div class="card-head">
        <h3 class="card-head__title">{{ prop.title }}</h3>
        <img src="@/assets/img/info-icon.png" />
      </div>
      <div class="card-body">
        <div class="card-content__left">
          <div
            class="pill pill-primary"
            v-bind:class="{
              'pill-blue': prop.id === 1,
              'pill-green': prop.id === 2,
              'pill-orange': prop.id === 3,
              'pill-violet': prop.id === 4,
            }"
          >
            <span>20%</span>
            <img
              v-bind:class="{ rotate90: prop.increase == false }"
              src="@/assets/img/arrow-icon.png"
            />
          </div>
        </div>
        <div class="card-content__right">
          <div class="sales-content">
            <p class="text-secondary">{{ prop.dscp1 }}</p>
            <section class="sales">
              <img src="@/assets/img/ph-icon.png" />
              <span>{{ prop.sale1 }}</span>
            </section>
          </div>
          <div class="sales-content">
            <p class="text-secondary">{{ prop.dscp2 }}</p>
            <section class="sales">
              <img src="@/assets/img/ph-icon.png" />
              <span>{{ prop.sale2 }}</span>
            </section>
          </div>
        </div>
      </div>
      <div class="card-footer">
        <div class="card-footer__container" style="padding: 13px 20px">
          <p class="text-gray__light">
            <small>{{ prop.foottext }}</small>
          </p>
          <small class=" ml-auto">
            <section class="sales" v-if="prop.id === 1">
              <img src="@/assets/img/ph-icon.png" />
              <span class="text-gray__light font-normal">{{ prop.total }}</span>
            </section>
          </small>
        </div>
      </div>
    </div>
  </Fragment>
</template>
<script>
import { Fragment } from "vue-fragment";
export default {
  components: {
    Fragment
  },
  props: ["propss"]
};
</script>
<style lang="scss" scoped>
.card {
  background: #f8faf9;
  position: relative;
  border-radius: 4px;
  box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.13);
  transition: ease-in-out 0.2s;
  &:focus {
      box-shadow: 0 2px 10px rgba(20,59,255,86%);
      background: #fff;
  }
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
    min-height: 120px;
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
.pill-blue {
  background: #7d9ffc;
  color: #fff;
}
.pill-green {
  background: #8bdcb7;
  color: #fff;
}
.pill-orange {
  background: #f6c37f;
  color: #fff;
}
.pill-violet {
  background: #c9a6e9;
  color: #fff;
}
.sales {
  margin-top: 3px;
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
  max-width: 115px;
  margin-bottom: 3px;
}
.sales-content {
  margin-top: 7px;
}
.ml-auto {
  margin-left: auto;
}
small {
  color: #808080;
  font-size: 0.7em;
  font-weight: normal;
}
.text-gray__light {
  color: #b8b9ba;
}
.rotate90 {
  transform: rotate(180deg);
}
.rotate0 {
  transform: rotate(0deg);
}
</style>
