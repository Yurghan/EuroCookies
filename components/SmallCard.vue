<template>
  <NuxtLink :to="`/products/${card.id}`" class="card-container">
    <img
      :src="require(`@/assets/images/${card.image || 'cookie1-min.png'}`)"
      alt="fe"
      class="image"
    />
  </NuxtLink>
</template>

<script>
export default {
  props: ["card"],
};
</script>

<style scoped>
.card-container {
  width: 24%;
  height: 12.5rem;
  padding: 1rem;
  border: 1px solid #000;
  border-radius: 0.5rem;
  overflow: hidden;
  margin-bottom: 1.5rem;
  cursor: pointer;
}

.card-container:hover {
  transition: all 0.1s ease-in-out;
  padding: 0.5rem;
}

.image {
  width: 100%;
  height: 100%;
}
</style>
