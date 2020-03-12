<template>
  <div class="performance-container">
    <div class="card-container">
      <PerformanceCard :title="cardtitle1" :dataProps="branchData" />
      <PerformanceCard :title="cardtitle2" :dataProps="rewardsData" />
    </div>
  </div>
</template>

<script>
import PerformanceCard from './PerformanceCard.vue';
export default {
  components: {
    PerformanceCard
  },
  data: () => {
    return {
      cardtitle1: 'Branch Performance',
      cardtitle2: 'Reward Performance',
      branchData: [
        {
          id: 1,
          branch: "Makati",
          totalSales: 5000,
          percentage: 20,
          increase: true
        },
        {
          id: 2,
          branch: "BGC Taguig",
          totalSales: 4000,
          percentage: 10.52,
          increase: true
        },
        {
          id: 3,
          branch: "Mall of Asia Pasay",
          totalSales: 3000,
          percentage: 10,
          increase: true
        },
        {
          id: 4,
          branch: "Quezon City",
          totalSales: 2000,
          percentage: 5,
          increase: false
        },
        {
          id: 5,
          branch: "Greenhills",
          totalSales: 1000,
          percentage: 2,
          increase: true
        }
      ],
      rewardsData: [
        {
          id: 1,
          badge: "Reward 1",
          totalSales: 5000,
          percentage: 20,
          increase: true
        },
        {
          id: 2,
          badge: "Reward 2",
          totalSales: 5000,
          percentage: 20,
          increase: true
        },
        {
          id: 3,
          badge: "Reward 3",
          totalSales: 5000,
          percentage: 20,
          increase: true
        },
        {
          id: 4,
          badge: "Reward 4",
          totalSales: 5000,
          percentage: 20,
          increase: false
        },
        {
          id: 5,
          badge: "Reward 5",
          totalSales: 5000,
          percentage: 20,
          increase: true
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.performance-container {
  padding: 20px 40px 60px;
  max-width: 1500px;
  margin: auto;
}
.card-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 40px;
    @media only screen and (max-width: 900px) {
    grid-template-columns: repeat(2, 1fr);
  }
  @media only screen and (max-width: 426px) {
    grid-template-columns: 1fr;
  }
}
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
.card-body {
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
  div {
    // border: 1px solid black
  }
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
</style>
