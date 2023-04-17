<template>
  <div>
    <h1>Character</h1>
    <p>Character page</p>
    <button></button>
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
