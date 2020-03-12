<template>
  <div class="chart-container">
      <div class="columns">
          <div class="column">
              <chartjs-bar :labels="labels" :data="dataset" :bind="true" />
          </div>
      </div>
  </div>
</template>
<script>
    export default {
        data: () => {
            return {
                dataentry: null,
                datalabel: null,
                labels: [
                    'Aug'
                ],
                dataset: [1,2,3,4,5]
            }
        },
        methods: {
            addData: function addData() {
                this.dataset.push(this.dataentry);
                this.labels.push(this.datalabel);
                this.datalabel='';
                this.dataentry='';
            }
        }
    }
</script>

<style lang="scss" scoped>
.chart-container {
  padding: 20px 30px;
}
</style>
