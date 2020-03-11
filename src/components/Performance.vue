<template>
  <div class="performance-container">
    <div class="card-container">
        <div class="card">
            <div class="card-header">
                <p><strong>Branch Performance</strong>  <span>?</span></p>
            </div>
            <div class="card-body">
                <div>
                    <ul style="display: flex;">
                        <li>1</li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="card">
            <div class="card-header">
                <p><strong>Reward Performance</strong>  <span>?</span></p>
            </div>
            <div class="card-body">
                <div>
                    <ul style="display: flex;">
                        <li>1</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      title: "Hello from Performance",
      branchData: [
        {
          branch: "Makati",
          totalSales: 5000,
          percentage: 20
        },
        {
          branch: "BGC Taguig",
          totalSales: 4000,
          percentage: 10.52
        },
        {
          branch: "Mall of Asia Pasay",
          totalSales: 3000,
          percentage: 10
        },
        {
          branch: "Quezon City",
          totalSales: 2000,
          percentage: 5
        },
        {
          branch: "Greenhills",
          totalSales: 1000,
          percentage: 2
        }
      ],
      rewardsData: [
        {
          badge: "Reward 1",
          totalSales: 5000,
          percentage: 20
        },
        {
          badge: "Reward 2",
          totalSales: 5000,
          percentage: 20
        },
        {
          badge: "Reward 3",
          totalSales: 5000,
          percentage: 20
        },
        {
          badge: "Reward 4",
          totalSales: 5000,
          percentage: 20
        },
        {
          badge: "Reward 5",
          totalSales: 5000,
          percentage: 20
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.performance-container {
  padding: 40px;
  max-width: 1500px;
  margin: auto;
  border: 1px solid black;
}
.card-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 20px;
    border: 1px solid black;
}
.card {
    background: #fff;
    border: 1px solid black;
}
</style>
