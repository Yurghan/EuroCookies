<template>
  <div>
    <div v-if="myItems.length > 0">
      <MyItem v-for="myItem in myItems" :key="myItem.id" :item="myItem" />
    </div>
    <div v-else>
      <h3>Add some cookies</h3>
    </div>
  </div>
</template>

<script>
export default {
  layout: "no-nav",
  data() {
    return {
      myItems: this.$store.state.myRentals,
    };
  },
};
</script>

<style scoped>
h3 {
  margin-top: 2rem;
}
</style>
