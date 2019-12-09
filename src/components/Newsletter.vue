<template>
  <section class="newsletter">
    <h3 class="newsletter__headline">Join our newsletter.</h3>
    <h5 class="newsletter__byline">Stay up to date on all the latest releases.</h5>
    <form action="#" class="newsletter__form">
      <input type="text" class="newsletter__input">
      <button class="newsletter__submit">Join</button>
    </form>
  </section>
</template>

<script>

export default {
  name: 'Newsletter',
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

<style lang="scss" scoped>

.newsletter {
  padding: 140px 0;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center 30%;
  background-image: 
    linear-gradient(
      to right bottom, rgba(255, 167, 81, 0.9), rgba(255, 226, 89, 0.75)),
      url(../assets/images/lifestyle/lifestyle-aerial-beach.jpg);
  
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  &::before {
    content: '';
    background-image: url('../assets/images/textures/tear-overlay-bottom.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 50% 50%;
    height: 10px;
    width: 100%;
    position: absolute;
    left: 0;
    top: 0;
    pointer-events: none;
    z-index: 20;
    transform: rotate(180deg);
  }

  &__headline,
  &__byline {
    color: rgba(47, 54, 64, 1);
  }

  &__headline {
  text-align: center;
  font-size: 2em;
  letter-spacing: 1px;
  position: relative;
  margin: 0;

    &::before {
      content: " ";
      position: absolute;
      width: 50px;
      height: 4px;
      background: var(--red);
      margin-top: -20px;
      left: 50%;
      transform: translateX(-50%);
    }
  }

  &__byline {
    font-size: 1.5em;
    font-weight: 100;
    margin: 6px 0 45px 0;
    text-align: center;
  }

  &__form {
    width: 40%;
    max-width: 600px;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
    box-shadow: 0px 3px 25px rgba(0, 0, 0, 0.25);
    border-radius: 30px;
  }

  &__input,
  &__submit {
    height: 50px;
    border: none;
    font-family: inherit;
    font-size: 0.9em;
  }

  &__input {
    flex: 4;
    padding: 0 0 0 2em;
    border-radius: 30px 0 0 30px;
  }

  &__submit {
    // height: 50px;
    flex: 1;
    width: 180px;
    padding: 0.85em 2.5em;
    color: var(--offWhite);
    background: var(--red);
    text-transform: uppercase;
    letter-spacing: 2px;
    cursor: pointer;
    border-radius: 0 30px 30px 0;
  }

}


</style>
