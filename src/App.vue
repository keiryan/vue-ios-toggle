<template>
  <div class="container">
    <ButtonToggle />
  </div>
</template>

<script>
import ButtonToggle from "./components/buttonToggle.vue";

export default {
  name: "App",
  components: {
    ButtonToggle,
  },
};
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */

body { 
  margin: 0;
  padding: 0;
  font-family: sans-serif;
}

.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100vw;
  background-color: #000;
  color: #fff;
}
</style>