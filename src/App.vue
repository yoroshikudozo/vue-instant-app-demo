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

ul,
li {
  margin: 0;
  padding: 0;
  list-style: none;
}

#app {
  height: 100%;
  background: black;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.title {
  h1 {
    margin: 0 0 24px;
    padding: 8px 0 7px;
    border-bottom: 1px solid #666;
    font-size: 24px;
    font-weight: normal;
  }
}
</style>
