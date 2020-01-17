<template>
  <div id="app">
    <Landing />
  </div>
</template>

<script>
import Landing from "./views/Landing";

export default {
  name: "app",
  components: {
    Landing
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  padding: 0;
}
</style>
