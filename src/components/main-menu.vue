<template>
  <h1>Dungeon Rush</h1>
  <p>Welcome traveler.</p>
  <div class="content">
    <div class="top">
      <div class="map-wrapper">
        <button class="map">
          <img src="../assets/map_cleanup.png" alt="map icon" />
        </button>
      </div>
      <div class="shop-wrapper">
        <button class="shop">
          <img src="../assets/shop.png" alt="shop icon" />
        </button>
      </div>
    </div>
    <div class="bottom">
      <div class="character-wrapper">
        <button class="character">
          <img src="../assets/knight.png" alt="character icon" />
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "mainMenu",
};
</script>

<style scoped>
@font-face {
  font-family: diamond-dust;
  src: url("../assets/font/DiamondDust-m3a9.ttf");
}

.content {
  overflow: hidden;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.top {
  display: flex;
  flex-direction: row;
  margin-bottom: 30px;
}

.map,
.shop,
.character {
  height: 400px;
}

.map {
  margin-right: 50px;
}

.map:hover,
.shop:hover,
.character:hover {
  cursor: pointer;
  transform: rotate(1deg);
  transition: ease-in-out 0.3s;
}

.map img,
.shop img,
.character img {
  height: 100%;
  width: 300px;
}

h1,
p {
  text-align: center;
  font-family: "diamond-dust";
}

h1 {
  margin-top: -10px;
  margin-bottom: -20px;
  font-size: 40px;
}

p {
  font-size: 25px;
}
</style>
