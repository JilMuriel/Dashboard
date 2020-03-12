<template>
  <div class="selectdiv ">
    <label>
      <select>
        <option selected> {{ title }} </option>
        <option v-for="drpData of drpData" :key="drpData.title">
            {{drpData.itemTitle}}
        </option>
      </select>
    </label>
  </div>
</template>
<script>
export default {
  props: ["title", "drpData"]
};
</script>

<style lang="scss" scoped>
.selectdiv {
  position: relative;
  /*Don't really need this just for demo styling*/
  /*   float: left;
  
  margin: 50px 33%; */
  //   max-width: 300px;
  min-width: 180px;
  margin-right: 10px;
}

.selectdiv:after {
  content: "\f078";
  font: normal normal normal 12px/1 FontAwesome;
  color: #6f6f6f;
  right: 10px;
  top: 8px;
  height: 10px;
  padding: 10px 0px 0px 8px;
  position: absolute;
  pointer-events: none;
}

/* IE11 hide native button (thanks Matt!) */
select::-ms-expand {
  display: none;
}

.selectdiv select {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  /* Add some styling */

  display: block;
  width: 100%;
  max-width: auto;
  height: 38px;
  border-radius: 4px;
  margin: 5px 0px;
  padding: 0px 15px;
  font-size: 0.8em;
  line-height: 1.75;
  color: #333;
  background-color: #ffffff;
  background-image: none;
  -ms-word-break: normal;
  font-weight: 600;
  word-break: normal;
    box-shadow: 0 1px 3px rgba(115, 111, 111, 0.12);
    border: none;
}
</style>
