<template>
  <div class="sand">
    <img src="./assets/sand.svg">
  </div>

  <section class="kelp">
    <img src="./assets/kelp.svg">
    <img src="./assets/ghost-kelp.svg">
    <img src="./assets/blue-kelp.svg">
  </section>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'Kelp',
  components: {
//    HelloWorld
  }
}
</script>

<style>
  body {
    background-image: url('./assets/background.svg'), linear-gradient(#0444b1, #2d1d8f);
    background-repeat: no-repeat;
    background-size: cover;
    color: #fff;
    min-height: 100vh;
    padding: 0;
    margin: 0;
    max-height: 100vh;
    overflow: hidden;
  }

  .sand {
    position: absolute;
    width: 100%;
    bottom: 0;
    z-index: 2;
  }

  .kelp {
    position: absolute;
    width: 100%;
    bottom: 0.5em;
  }

  .kelp img {
    max-height: 80vh;
    padding: 0 4em;
    transform-origin: bottom center;
    animation-name: sway;
    animation-duration: 30s;
    animation-iteration-count: infinite;
  }

  @keyframes sway {
    0% { transform: rotate(15deg); }
    50% { transform: rotate(-15deg); }
    100% { transform: rotate(15deg); }
  }
</style>
