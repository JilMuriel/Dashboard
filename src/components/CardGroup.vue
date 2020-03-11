<template>
  <section class="card-container">
    <div v-for="cardData in cardDatas" :key="cardData.id" class="card">
      <div class="card-head">
        <h3>{{ cardData.title }}</h3>
      </div>
      <div class="card-body">
        <p>{{ cardData.body }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data: () => {
    return {
      title: "Hello from card group",
      cardDatas: [
        {
          id: 1,
          title: "Sales",
          body:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero autem necessitatibus perspiciatis quasi amet culpa fugiat impedit voluptates itaque nobis tenetur nihil deserunt, sint esse similique dicta. Aliquid, enim ut!"
        },
        {
          id: 2,
          title: "engagement",
          body: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
        },
        {
          id: 3,
          title: "aquisition",
          body:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.Vero autem necessitatibus perspiciatis quasi amet culpa fugiat impedit voluptates itaque nobis tenetur nihil deserunt"
        },
        {
          id: 4,
          title: "rewards program",
          body:
            "Vero autem necessitatibus perspiciatis quasi amet culpa fugiat impedit voluptates itaque nobis tenetur nihil deserunt"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.card-container {
  padding: 20px;
  max-width: 1500px;
  margin: auto;

  display: grid;
  grid-gap: 20px;
  grid-template-columns: repeat(4, 1fr);

  border: 1px solid black;
}
.card {
  border: 1px solid black;
  background: white;
  .card-head {
    padding: 10px 20px;
    border: 1px solid black;
  }
  .card-body {
    padding: 20px;
    border: 1px solid black;
  }
}
</style>
