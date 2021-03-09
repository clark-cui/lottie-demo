<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
    <div id="svgContainer"></div>
    <!-- <router-view /> -->
  </div>
</template>

<script lang="ts">
import lottie from "lottie-web";
export default {
  mounted() {
    const svgContainer = document.getElementById("svgContainer");
    const animItem = lottie.loadAnimation({
      wrapper: svgContainer,
      animType: "svg",
      loop: true,
      path:
        "https://labs.nearpod.com/bodymovin/demo/markus/isometric/markus2.json",
    });
  },
};
</script>

<style lang="scss">
html {
  margin: 0;
  padding: 0;
  background-color: #1e1c26;
}

body,
html {
  width: 100%;
  height: 100%;
  overflow: hidden;
  background-color: #000;
  margin: 0;
}

#svgContainer {
  max-width: 100%;
  max-height: 100%;
  background-color: #1e1c26;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  margin: auto;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
