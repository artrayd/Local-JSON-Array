<template>
  <ul class="alphabet">
    <li v-for="letter in letters" :key="letter.name">
      <img :src="letterIcon(letter.path)" alt="" />
      <span>{{ letter.name }}</span>
      <div class="tooltip">{{ letter.alt }}</div>
    </li>
  </ul>
</template>

<script>
// Importing array from our JSON file
import json from "@/assets/letters/greek-alphabet.json";

export default {
  name: "Alphabet",
  data: function() {
    return {
      letters: json.letters, // passing array data into Vue
    };
  },
  methods: {
    letterIcon: function(path) {
      return require("@/" + path);
    },
  },

  mounted: function() {
    // Checking if everything works, delete this right after you see that everything works
    // console.log(this.letters);
  },
};
</script>

<style lang="sass" scoped>
.alphabet
    padding: 0
    margin: 0
</style>
