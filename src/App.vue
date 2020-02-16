<template>
  <div id="app">
    <Swiper msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import Swiper from "./components/Swiper.vue";

export default {
  name: "App",
  components: {
    Swiper
  }
};
</script>

<style lang="scss">
html {
  height: 100%;
  background: black;
}

body {
  height: 100%;
  margin: 0;
  padding: 0;
  background: black;
}

#app {
  height: 100%;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: black;
}
</style>
