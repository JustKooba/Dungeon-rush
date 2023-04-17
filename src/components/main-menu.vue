<template>
  <div :style="{ display: mainMenuDisplay }">
    <h1>Dungeon Rush</h1>
    <p>Welcome traveler.</p>
    <div class="content">
      <div class="top">
        <div class="map-wrapper">
          <button class="map">
            <img
              src="../assets/map_cleanup.png"
              alt="map icon"
              @click="mapClick"
            />
          </button>
        </div>
        <div class="shop-wrapper">
          <button class="shop">
            <img src="../assets/shop.png" alt="shop icon" @click="shopClick" />
          </button>
        </div>
      </div>
      <div class="bottom">
        <div class="character-wrapper">
          <button class="character">
            <img
              src="../assets/knight.png"
              alt="character icon"
              @click="characterClick"
            />
          </button>
        </div>
      </div>
    </div>
  </div>
  <character-main
    :style="{ display: characterDisplay }"
    v-on:characterClickBack="characterClick"
  />
  <shop-main :style="{ display: shopDisplay }" v-on:shopClickBack="shopClick" />
  <map-main :style="{ display: mapDisplay }" v-on:mapClickBack="mapClick" />
</template>

<script>
import shopMain from "./shop-main.vue";
import characterMain from "./character-main.vue";
import mapMain from "./map-main.vue";
export default {
  name: "mainMenu",

  data() {
    return {
      characterDisplay: "none",
      mainMenuDisplay: "block",
      shopDisplay: "none",
      mapDisplay: "none",
    };
  },

  components: {
    characterMain,
    shopMain,
    mapMain,
  },

  methods: {
    mapClick() {
      console.log("map clicked");
      if (this.mapDisplay === "none" || this.mainMenuDisplay === "block") {
        this.mapDisplay = "block";
        this.mainMenuDisplay = "none";
      } else {
        this.mapDisplay = "none";
        this.mainMenuDisplay = "block";
      }
    },
    shopClick() {
      console.log("shop clicked");
      if (this.shopDisplay === "none" || this.mainMenuDisplay === "block") {
        this.shopDisplay = "block";
        this.mainMenuDisplay = "none";
      } else {
        this.shopDisplay = "none";
        this.mainMenuDisplay = "block";
      }
    },
    characterClick() {
      console.log("character clicked");
      if (
        this.characterDisplay === "none" ||
        this.mainMenuDisplay === "block"
      ) {
        this.characterDisplay = "block";
        this.mainMenuDisplay = "none";
      } else {
        this.characterDisplay = "none";
        this.mainMenuDisplay = "block";
      }
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

@media (max-width: 670px) {
  .content {
    display: flex;
  }
  .top {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .map {
    margin-right: 0;
    margin-bottom: 30px;
  }
}
</style>
