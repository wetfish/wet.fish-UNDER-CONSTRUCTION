<template>
  <div class="bubble"></div>
</template>

<script>
  export default {

  }
</script>

<style lang="scss">
  .bubble {
    border: 1px solid rgba(255, 255, 255, 0.4);
    background-color: rgba(255, 255, 255, 0.2);
    width: 1.4em;
    height: 1.4em;
    border-radius: 100%;
    margin-left: 20em;
    z-index: 10;
    position: absolute;
    animation: float 3s, wiggle 2s;
    animation-iteration-count: infinite;
    animation-timing-function: ease-in;
  }

  .floating {

  }

  @keyframes wiggle {
    0% {
      width: 1.4em;
      height: 1.4em;
    }

    25% {
      width: 1.8em;
      height: 1.2em;
    }

    50% {
      width: 1.3em;
      height: 1.9em;
    }

    75% {
      width: 2em;
      height: 1.1em;
    }

    100% {
      width: 1.4em;
      height: 1.4em;
     }
  }

  @keyframes float {
    0% { transform: translateY(100vh) }
    100% { transform: translateY(-10vh) }
  }
</style>
