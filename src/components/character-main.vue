<template>
  <div class="content">
    <h1>Customize yourself, traveler.</h1>
    <button @click="characterClick" class="back">
      <img src="../assets/back.svg" />
    </button>
    <div class="bottom">
      <div class="inv-wrap">
        <h3>Inventory</h3>
        <div class="inventory">
          <div
            v-for="item in inventory"
            :key="item.index"
            class="item-box"
          ></div>
        </div>
      </div>
      <div class="char-wrap">
        <h3>Character Equipment</h3>
        <div class="character">
          <div
            v-for="slot in character"
            :key="slot.index"
            class="item-box"
          ></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import inventoryData from "./data/inventory.json";
import characterEqData from "./data/characterEq.json";

export default {
  name: "characterMain",
  data() {
    return {
      inventory: inventoryData.inventory,
      character: characterEqData.eq,
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

h3 {
  font-family: "Courier New", Courier, monospace;
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

.inventory {
  display: grid;
  grid-template-columns: repeat(5, 100px);
  grid-template-rows: repeat(4, 100px);
  justify-content: center;
  margin-top: 15px;
}

.character {
  display: grid;
  grid-template-columns: repeat(2, 100px);
  grid-gap: 12px;
  justify-content: center;
}

.item-box {
  width: 80px;
  height: 80px;
  border: 1px solid rgb(204, 204, 204);
  display: flex;
  justify-content: center;
  align-items: center;
}

.bottom {
  display: flex;
  justify-content: space-around;
}
</style>
