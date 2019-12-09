<template>
  <header class="hero">
    <h1 class="hero__headline">Set yourself apart.</h1>
    <a href="/" class="hero__cta">Shop new arrivals</a>
  </header>
</template>

<script>

export default {
  name: 'Hero',
  props: {
    msg: String
  },
  data() {
    return {
      
    }
  },
  methods: {

  },

}
</script>

<style lang="scss">

.hero {
  height: 50vh;
  width: 100%;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-size: cover;
  background-repeat: no-repeat;
  background-origin: content-box;
  background-position: center;
  background-image: 
    linear-gradient(
      to right bottom, rgba(26,41,128,0.9), rgba(38,208,206,0.65)),
      url(../assets/images/lifestyle/lifestyle-jumping.jpg);
  z-index: 20;
  
  &::after {
    content: '';
    background-image: url('../assets/images/textures/tear-overlay-bottom.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 50% 50%;
    height: 10px;
    width: 100%;
    position: absolute;
    left: 0;
    bottom: 0;
    pointer-events: none;
    z-index: 30;
  }

  &__headline {
    color: var(--offWhite);
    font-size: 90px;
    text-align: center;
    margin: 0 0 35px 0;
  }

  &__cta {
    color: var(--offWhite);
    text-decoration: none;
    text-transform: uppercase;
    font-size: 18px;
    letter-spacing: 2px;
    border-radius: 30px;
    padding: 0.7em 2em;
    transition: all 300ms ease;
    position: relative;
    overflow: hidden;
    background: lighten(#c13515, 3%);
    box-shadow: 0px 3px 25px rgba(0, 0, 0, 0.25);

&:hover {
      background: lighten(#c13515, 6%);
    }
  }

}


</style>
