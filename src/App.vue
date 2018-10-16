<template>
  <div id="app">
    <Strips/>
  </div>
</template>

<script>
import Strips from "./components/Strips";

export default {
  name: "App",
  components: {
    Strips
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
  margin-top: 60px;
}
</style>
