<template>
  <section>
    <h2>Greek Alphabet</h2>
    <span>{{ lettersAmount }} letters</span>
    <ul class="alphabet">
      <li v-for="letter in letters" :key="letter.name">
        <img :src="letterIcon(letter.path)" alt="" />
        <p>{{ letter.name }}</p>
        <div class="tooltip">{{ letter.alt }}</div>
      </li>
    </ul>
  </section>
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

  computed: {
    lettersAmount: function() {
      return this.letters.length;
    },
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
section
    display: flex
    flex-direction: column
    align-items: flex-start

    h2
        margin-bottom: 4px

    span
        color: #A6A6AC

    .alphabet
        padding: 0
        margin: 0
        margin-top: 40px
        display: grid
        grid-template-columns: repeat( auto-fill, minmax(140px, 1fr) )

        column-gap: 72px
        row-gap: 32px
        width: 100%


        li
            list-style: none
            display: flex
            align-items: center
            position: relative
            border-radius: 12px
            transition: backround .2s
            width: 100%

            p
                margin: 0
                margin-left: 12px

            .tooltip
                position: absolute
                top: -32px
                background: rgba(0,0,0,0.85)
                color: #fff
                font-size: 14px
                padding: 4px 16px
                border-radius: 12px
                opacity: 0
                transition: opacity .2s

            &:hover .tooltip
                opacity: 1
</style>
