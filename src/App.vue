<template>
  <div>
    <main-menu />
  </div>
</template>

<script>
import mainMenu from "./components/main-menu.vue";
export default {
  name: "App",
  components: {
    mainMenu,
  },
};
</script>

<style>
body {
  background-color: #121212;
  color: #fff;
}
</style>
