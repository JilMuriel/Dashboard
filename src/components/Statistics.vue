<template>
  <div class="container">
    <div class="container-head">
      <section class="date-picker">
        <Dropdown :title="dropdownDay" :drpData="dropdownDatas" />
        <date-picker
          v-model="value1"
          type="date"
          range
          placeholder="Select date range"
        ></date-picker>
      </section>
    </div>
    <div class="container-body">
      <div class="card">
        <!-- Card Header -->
        <div class="card-header">
          <section class="card-header__title">
            <p>
              <strong>Sales Overview</strong>
            </p>
            <img src="@/assets/img/info-icon.png" />
          </section>
          <div class="card-header__dropdown-group">
            <Dropdown :title="dropdownTransaction" :drpData="dropdownDatas" />
            <Dropdown :title="dropdownBranches" :drpData="dropdownDatas" />
          </div>
        </div>
        <!-- Card Header -->
        <!-- Card Body -->
        <div class="chart-header">
          <h4 class="chard-header_title">Total:</h4>
          <section class="pill-container">
            <Pill :dataPill="salesData" :type="primary" />
            <Pill :dataPill="revenueData" :type="secondary" />
            <Pill :dataPill="generatedData" :type="violet" />
            <Pill :dataPill="pointData" :type="violet" />
          </section>
          <section class="ind-container">
            <Idt :propsData="salesData" :type="primary" />
            <Idt :propsData="revenueData" :type="secondary" />
          </section>
        </div>
        <!-- Card Body -->
        <Chart />
      </div>
    </div>
  </div>
</template>
<script>
import DatePicker from "vue2-datepicker";
import "vue2-datepicker/index.css";
import Dropdown from "./Dropdown";
import Pill from "./Pill";
import Idt from "./Idt";
import Chart from "./Chart.vue";
export default {
  components: {
    DatePicker,
    Dropdown,
    Pill,
    Idt,
    Chart
  },
  data: () => {
    return {
      value1: [new Date(2019, 1, 1), new Date(2020, 1, 1)],
      dropdownDay: "Last 7 Days",
      dropdownTransaction: "All Transactions",
      dropdownBranches: "All Branches",
      dropdownDatas: [
        {
          itemTitle: "Dropdown value 01"
        },
        {
          itemTitle: "Dropdown value 02"
        },
        {
          itemTitle: "Dropdown value 02"
        }
      ],
      primary: "primary",
      secondary: "secondary",
      violet: "violet",
      salesData: [
        {
          id: 123,
          title: "Sales",
          amount: "Php 10,000.00"
        }
      ],
      revenueData: [
        {
          id: 123,
          title: "Revenue",
          amount: "Php 10,000.00"
        }
      ],
      generatedData: [
        {
          id: 123,
          title: "Generated Points",
          amount: "1000 Points"
        }
      ],
      pointData: [
        {
          id: 123,
          title: "Used Points",
          amount: "1000 Points"
        }
      ]
    };
  }
};
</script>
<style lang="scss" scoped>
.container {
  padding: 0px 40px;
  max-width: 1500px;
  margin: auto;

  .container-head {
    display: flex;
    flex-direction: row;

    margin-bottom: 35px;
  }
}
.container-body {
  background: #fff;
}
.mx-datepicker-range {
  width: auto;
}
.card {
  box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.13);
  border-radius: 6px;
}
.card-header {
  display: flex;
  align-items: center;
  background: #f7f8fc;
  padding: 20px 30px;
    flex-wrap: wrap;
}
.card-header__dropdown-group {
  margin-left: auto;
  display: flex;
  align-items: center;
    flex-wrap: wrap;
}
.card-header__title {
  display: flex;
  align-items: center;
  img {
    margin-left: 5px;
  }
}
.date-picker {
  display: flex;
  align-items: center;
    flex-wrap: wrap;
}
.chart-header {
  padding: 20px 30px;
  display: flex;
  align-items: flex-end;
    flex-wrap: wrap;
  @media only screen and (max-width: 768px) {
    align-items: center;  
  }
}
.chard-header_title {
  margin-right: 30px;
}
.pill-container {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  div {
    margin-right: 10px;
  }
}
.ind-container {
  display: flex;
  align-items: center;
  margin-left: auto;
  @media only screen and (max-width: 768px) {
    margin-left: 0;
    margin-top: 10px;
  }
  div {
    margin-right: 5px;
  }
}
</style>
