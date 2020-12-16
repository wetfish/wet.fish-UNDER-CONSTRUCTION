<template>
  <img class="fish" :class="species" :src="speciesUrl">
</template>

<script>
  export default {
    props: {
      species: {
        type: String,
        default: "blue" // Blue, Pink, Shark
      },

      height: Number,
      width: Number,
      flipped: Boolean
    },

    computed: {
      speciesUrl() {
        if(this.species == 'pink') {
          return require("../assets/pink-fish.svg");
        } else if(this.species == 'shark') {
          return require("../assets/shark.svg");
        } else {
          return require("../assets/blue-fish.svg");
        }
      }
    }
  }
</script>

<style lang="scss">
  .fish {
    &.blue {
      max-width: 50px;
    }

    &.pink {
      max-width: 200px;
    }

    &.shark {
      max-width: 700px;
    }
  }
</style>
