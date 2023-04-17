<template>
  <div>
    <h1>Map</h1>
    <p>Map page</p>
    <button @click="mapClick">Back</button>
  </div>
</template>

<script>
export default {
  methods: {
    mapClick() {
      this.$emit("mapClickBack");
    },
  },
};
</script>

<style></style>
