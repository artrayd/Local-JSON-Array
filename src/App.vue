<template>
  <div id="app">
    <Alphabet class="center" />
  </div>
</template>

<script>
import Alphabet from "./components/alphabet.vue";

export default {
  name: "App",
  components: {
    Alphabet,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
