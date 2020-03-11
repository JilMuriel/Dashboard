<template>
  <div class="container">
    <div class="container-head">
      <section>
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
          <p><strong>Sales Overview</strong> <span>icon</span></p>
          <div class="card-header__dropdown-group">
            <select>
              <option>All Transaction</option>
            </select>
            <select>
              <option>All Branches</option>
            </select>
          </div>
        </div>
        <!-- Card Header -->
      </div>
    </div>
  </div>
</template>
<script>
import DatePicker from "vue2-datepicker";
import "vue2-datepicker/index.css";

export default {
  components: {
    DatePicker,
  },
  data: () => {
    return {
      value1: [new Date(2019, 1, 1), new Date(2020, 1, 1)]
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
  .container-head {
    display: flex;
    flex-direction: row;
    border: 1px solid black;
    margin-bottom: 40px;
  }
}
.container-body {
  background: #fff;
  padding: 20px;
  border: 1px solid black;
}
.mx-datepicker-range {
  width: auto;
}

//card header select box
.card-header {
  display: flex;
  align-items: center;
}
.card-header__dropdown-group {
  margin-left: auto;
}
</style>
