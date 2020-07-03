<template>
  <div id="app">
    <Alphabet class="center" />

    <section class="title">
      <h1>This array was imported from the local JSON file.</h1>
      <p>
        This is an example of an exercise for VueJs learning purpose.
        <a href="#">Read VueJS Tutorial</a>
        Download this project from the
        <a href="https://github.com/artrayd/items-array-from-local-json"
          >GitHub repository</a
        >
      </p>
    </section>
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

<style lang="sass">
#app
  font-family: Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: center
  color: #2c3e50
  margin-top: 60px
  margin: 60px 18px 0 18px
  max-width: 960px
  width: 100%

body
  display: flex
  justify-content: center
  align-items: center

.center
  display: flex
  justify-content: center
  align-items: center
*
  box-sizing: border-box

  .title
    margin-top: 120px
    text-align: left
</style>
