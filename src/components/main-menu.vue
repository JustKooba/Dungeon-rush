<template>
  <h1>Dungeon Rush</h1>
  <p>Welcome traveler.</p>
  <div class="content">
    <div class="map">
      <button class="map">
        <img src="../assets/map_cleanup.png" alt="map icon" />
      </button>
    </div>
    <div class="shop"></div>
    <div class="character"></div>
  </div>
</template>

<script>
export default {
  name: "mainMenu",
};
</script>

<style scoped>
.content {
  overflow: hidden;
}
.map {
  height: 400px;
}

.map:hover {
  cursor: pointer;
  transform: rotate(1deg);
  transition: ease-in-out 0.3s;
}

.map img {
  height: 100%;
  width: 300px;
}
</style>
