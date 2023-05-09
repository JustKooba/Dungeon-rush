<template>
  <div class="content">
    <h1>Choose your destination, traveler</h1>

    <div class="dungeons">
      <div class="top">
        <div class="Mine">
          <div class="desc">
            <h2>Mine</h2>
            <p>Recommended level: <span class="num"> 0</span></p>
          </div>
        </div>

        <div class="Shadow-Crypts">
          <div class="desc">
            <h2>Shadow Crypts</h2>
            <p>Recommended level: <span class="num"> 10</span></p>
          </div>
        </div>

        <div class="Infernal-Stronghold">
          <div class="desc">
            <h2>Infernal Stronghold</h2>
            <p>Recommended level: <span class="num"> 20</span></p>
          </div>
        </div>
      </div>
      <div class="bottom">
        <div class="Cursed-Keep">
          <div class="desc">
            <h2>Cursed Keep</h2>
            <p>Recommended level: <span class="num"> 30</span></p>
          </div>
        </div>

        <div class="Abyssal-Labyrinth">
          <div class="desc">
            <h2>Abyssal Labyrinth</h2>
            <p>Recommended level: <span class="num"> 40</span></p>
          </div>
        </div>
      </div>
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

.top {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.bottom {
  margin-top: 10px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.Shadow-Crypts,
.Mine,
.Infernal-Stronghold,
.Cursed-Keep,
.Abyssal-Labyrinth {
  height: 400px;
  width: 300px;
  background-repeat: no-repeat;
  cursor: pointer;
  border: 2px solid #fff;
  margin-right: 10px;
  display: flex;
  justify-content: center;
  font-size: 25px;
  text-shadow: -1px -1px 0 #000, 1px -1px 0 #000, -1px 1px 0 #000,
    1px 1px 0 #000;
}

.Shadow-Crypts {
  background: url("../assets/crypts.png");
}

.Mine {
  background: url("../assets/mine.png");
}

.Infernal-Stronghold {
  background: url("../assets/infernal.png");
}

.Cursed-Keep {
  background: url("../assets/c-keep.png");
}

.Abyssal-Labyrinth {
  background: url("../assets/abyss.png");
}

.dungeons div div:hover {
  cursor: pointer;
  transform: rotate(1deg);
  transition: ease-in-out 0.3s;
}

.num {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}

p {
  margin-top: -30px;
}

.desc {
  display: flex;
  flex-direction: column;
  text-align: center;
}
</style>
