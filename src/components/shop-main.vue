<template>
  <div class="content">
    <h1>You need something, traveler?</h1>
    <button @click="shopClick" class="back">
      <img src="../assets/back.svg" />
    </button>
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

<style scoped>
@font-face {
  font-family: diamond-dust;
  src: url("../assets/font/DiamondDust-m3a9.ttf");
}

.content {
  font-family: "diamond-dust", sans-serif;
}

.back {
  background: transparent;
  position: absolute;
  width: 50px;
  border: none;
  cursor: pointer;
  top: 30px;
}

h1 {
  letter-spacing: 5px;
  text-align: center;
}
</style>
