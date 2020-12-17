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
    margin-top: 20em;
    position: absolute;
    animation: swim 20s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;

    &.blue {
      max-width: 70px;
    }

    &.pink {
      max-width: 200px;
    }

    &.shark {
      max-width: 700px;
    }
  }

  @keyframes swim {
    0% { transform: translateX(100vw) }
    100% { transform: translateX(-100vw); }
  }
</style>
