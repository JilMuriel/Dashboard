<template>
  <section class="card-container">
    <CardItem :propss="saleDatas" />
    <CardItem :propss="engagementData" />
    <CardItem :propss="acquisition" />
    <CardItem :propss="reward" />
  </section>
</template>

<script>
import CardItem from "./CardItem.vue";

export default {
  components: {
    CardItem
  },
  data: () => {
    return {
      saleDatas: [
        {
          id: 1,
          title: "Sales",
          dscp1: "Lifetime Sales",
          sale1: "175,000",
          dscp2: "Revenue Sales",
          sale2: "170,000",
          percentage: 20,
          increase: true,
          foottext: "Average Order Value",
          total: "1,000,000.00"
        }
      ],
      engagementData: [
        {
          id: 2,
          title: "Engagement",
          dscp1: "Lifetime SMS Engagements",
          sale1: "285",
          dscp2: "Daily Average",
          sale2: "57",
          increase: false,
          foottext: "20% decrease in 30 days"
        }
      ],
      acquisition: [
        {
          id: 3,
          title: "Acquisition",
          dscp1: "Registered Users",
          sale1: "285",
          dscp2: "Daily Average",
          sale2: "57",
          increase: true,
          foottext: "20% Increase in 30 days"
        }
      ],
      reward: [
        {
          id: 4,
          title: "Reward Program",
          dscp1: "Reward Redeemed",
          sale1: "175,000",
          dscp2: "Issued Rewards",
          sale2: "175, 000",
          increase: true,
          foottext: "20% Increase in 30 days"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.card-container {
  padding: 135px 40px 20px;
  max-width: 1500px;
  margin: auto;
  display: grid;
  grid-gap: 20px;
  grid-template-columns: repeat(4, 1fr);
  @media only screen and (max-width: 900px) {
    grid-template-columns: repeat(2, 1fr);
  }
  @media only screen and (max-width: 426px) {
    grid-template-columns: 1fr;
  }
}
</style>
