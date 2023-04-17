<template>
  <div>
    <h1>Shop</h1>
    <p>Shop page</p>
    <button @click="shopClick">Back</button>
  </div>
</template>

<script>
export default {
  name: "shopMain",

  methods: {
    shopClick() {
      this.$emit("shopClickBack");
    },
  },
};
</script>

<style></style>
