<template>
  <img :src="speciesUrl">
</template>

<script>
  export default {
    props: {
      species: {
        type: String,
        default: "green" // Green, Blue, Ghost
      },

      height: Number,
      width: Number,
      flipped: Boolean
    },

    computed: {
      speciesUrl() {
        if(this.species == 'blue') {
          return require("../assets/blue-kelp.svg");
        } else if(this.species == 'ghost') {
          return require("../assets/ghost-kelp.svg");
        } else {
          return require("../assets/green-kelp.svg");
        }
      }
    }
  }
</script>

<style lang="scss">

</style>
