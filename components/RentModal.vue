<template>
  <div>
    <b-button id="show-btn" @click="showModal">Order</b-button>

    <b-modal ref="my-modal" hide-footer title="Order a cookie">
      <div class="calendar-container">
        <div class="text-container">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Iusto
            distinctio reprehenderit tempore officiis ex aperiam sit dicta,
            deleniti cupiditate dolorum.
          </p>
        </div>
      </div>
      <b-button
        id="show-btn"
        variant="outline-danger"
        @click="
          () => {
            addItem(product.id);
            hideModal();
          }
        "
        >Order</b-button
      >
    </b-modal>
  </div>
</template>

<script>
import { mapMutations } from "vuex";

export default {
  props: ["product"],
  methods: {
    showModal() {
      this.$refs["my-modal"].show();
    },
    hideModal() {
      this.$refs["my-modal"].hide();
    },
    toggleModal() {
      this.$refs["my-modal"].toggle("#toggle-btn");
    },
    ...mapMutations(["addItem"]),
  },
};
</script>

<style scoped>
button {
  width: 100%;
  border: none;
  padding: 0.5rem;
  color: white;
  font-weight: 700;
  padding: 1rem 4rem;
  border-radius: 100rem;
  background-color: rgb(231, 81, 43);
  color: white;
  font-weight: 700;
  transition: 0.5s;
}
.calendar-container {
  padding: 1rem;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}
p {
  color: grey;
}
.text-container {
  padding: 0.5rem;
}
</style>
