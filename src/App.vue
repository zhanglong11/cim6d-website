<template>
  <Home msg="Welcome to Your Vue.js App" />
</template>

<script>
import Home from "./components/home";

export default {
  name: "App",
  components: {
    Home,
  },
};
</script>

<style lang="less">
html,
body {
  position: relative;
  height: 100%;
  padding: 0;
  margin: 0;
  background: #fff;
}
* {
  box-sizing: border-box;
  letter-spacing: 0.1rem;
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}
</style>
