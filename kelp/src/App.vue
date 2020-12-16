<template>
  <section class="sand">
    <img src="./assets/sand.svg">
  </section>

  <section class="kelp">
    <Kelp />
    <Kelp species="blue" />
    <Kelp species="ghost" />
    <Kelp species="blue" />
    <Kelp species="ghost" />
    <Kelp />
  </section>

  <section class="bubbles">
    <Bubble />
    <Bubble />
    <Bubble />
    <Bubble />
  </section>

  <section class="fishes">
    <Fish />
    <Fish species="pink" />
    <Fish species="shark" />
  </section>
</template>

<script>
  import Kelp from './components/Kelp.vue';
  import Bubble from './components/Bubble.vue';
  import Fish from './components/Fish.vue';

  export default {
    name: 'Ocean',
    components: {
      Kelp,
      Bubble,
      Fish
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
    position: relative;
    width: 100%;
    height: 100vh;
    z-index: 100;
  }

  .sand img {
    position: absolute;
    bottom: 0;
  }

  .kelp {
    position: absolute;
    width: 5000px;
    bottom: 0.5em;
  }

  .kelp img {
    max-height: 80vh;
    transform-origin: bottom center;
    animation-name: sway;
    animation-duration: 30s;
    animation-iteration-count: infinite;
  }

  .kelp img:nth-of-type(1) {
    animation-delay: 1s;
  }

  .kelp img:nth-of-type(2) {
    animation-delay: 2s;
  }

  .kelp img:nth-of-type(3) {
    animation-delay: 3s;
  }

  .bubbles {
    position: absolute;
    top: 0;
    min-height: 100vh;
    width: 100%;
  }

  .fishes {
    position: absolute;
    top: 0;
    width: 100%;
  }

  .bubble:nth-of-type(1) {
    animation-delay: 0.5s;
    margin-left: 18em;
  }

  .bubble:nth-of-type(2) {
    animation-delay: 1.5s;
    margin-left: 22em;
    font-size: 1.5em;
  }

  .bubble:nth-of-type(3) {
    animation-delay: 2s;
    margin-left: 24em;
  }

  @keyframes sway {
    0% { transform: rotate(15deg); }
    50% { transform: rotate(-15deg); }
    100% { transform: rotate(15deg); }
  }
</style>
