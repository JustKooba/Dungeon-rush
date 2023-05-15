<template>
  <div class="content">
    <h1>Customize yourself, traveler.</h1>
    <button @click="characterClick" class="back">
      <img src="../assets/back.svg" />
    </button>

    <div class="inventory">
      <div v-for="item in inventory" :key="item.index" class="item-box"></div>
    </div>
  </div>
</template>

<script>
import inventoryData from "./data/inventory.json";

export default {
  name: "characterMain",
  data() {
    return {
      inventory: inventoryData.inventory,
    };
  },
  methods: {
    characterClick() {
      this.$emit("characterClickBack");
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

h1 {
  letter-spacing: 5px;
  text-align: center;
}

.back {
  background: transparent;
  position: absolute;
  width: 50px;
  border: none;
  cursor: pointer;
  top: 10px;
}

.item-box {
  width: 80px;
  height: 80px;
  border: 1px solid rgb(204, 204, 204);
  margin: 5px;
}
</style>
