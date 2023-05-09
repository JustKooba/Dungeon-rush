<template>
  <div>
    <h1>Customize yourself, traveler.</h1>
    <p>Character page</p>
    <button @click="characterClick">Back</button>
  </div>
</template>

<script>
export default {
  name: "characterMain",

  methods: {
    characterClick() {
      this.$emit("characterClickBack");
    },
  },
};
</script>

<style></style>
