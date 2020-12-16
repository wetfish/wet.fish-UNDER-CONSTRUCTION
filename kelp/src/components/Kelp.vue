<template>
  <img v-if="species == 'green'" src="../assets/kelp.svg">
  <img v-if="species == 'blue'" src="../assets/blue-kelp.svg">
  <img v-if="species == 'ghost'" src="../assets/ghost-kelp.svg">
</template>

<script>
  export default {
    props: {
      species: {
        type: String,
        default: "green" // Green, Blue, Ghost
      },

      height: Number
    }
  }
</script>

<style lang="scss">

</style>
