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
        },
        {
          id: 2,
          title: "Engagement",
        },
         {
          id: 3,
          title: "Acquisition"
        },
                {
          id: 4,
          title: "Rewards Program",
        },
      ]
    };
  }
};
</script>

<style lang="scss" scoped>


</style>
