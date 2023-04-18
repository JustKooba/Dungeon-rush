<template>
  <div class="content">
    <h1>Choose your destination, traveler</h1>

    <div class="dungeons">
      <div class="Mine"></div>

      <div class="Shadow-Crypts"></div>

      <div class="Infernal-Stronghold"></div>

      <div class="Cursed-Keep"></div>

      <div class="Abyssal-Labyrinth"></div>
    </div>
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

.dungeons {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  flex-wrap: wrap;
}

.Mine {
  background: url("../assets/mine.jpg");
  height: 400px;
  width: 300px;
  background-repeat: no-repeat;
}

.Shadow-Crypts {
  background: url("../assets/crypts.png");
  height: 400px;
  width: 300px;
  background-repeat: no-repeat;
}
</style>
