<template>
  <section>
    <CardItem v-bind:salesData="saleDatas" />
  </section>
</template>

<script>
import CardItem from './CardItem.vue'

export default {
  components: {
    CardItem,
  },
  data: () => {
    return {
      title: "Hello from card group",
      saleDatas: [
        {
          id: 1,
          title: "Sales",
          body:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero autem necessitatibus perspiciatis quasi amet culpa fugiat impedit voluptates itaque nobis tenetur nihil deserunt, sint esse similique dicta. Aliquid, enim ut!"
        },
        {
          id: 1,
          title: "Sales",
          body:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero autem necessitatibus perspiciatis quasi amet culpa fugiat impedit voluptates itaque nobis tenetur nihil deserunt, sint esse similique dicta. Aliquid, enim ut!"
        },
      ]
    };
  }
};
</script>

<style lang="scss" scoped>


</style>
