<template>
  <footer class="footer">
    <div class="footer__content">
      <ul class="column">
        <li><a href="#">Footer link</a></li>
        <li><a href="#">Footer link</a></li>
        <li><a href="#">Footer link</a></li>
        <li><a href="#">Footer link</a></li>
        <li><a href="#">Footer link</a></li>
      </ul>
      <ul class="column">
        <li><a href="#">Footer link</a></li>
        <li><a href="#">Footer link</a></li>
        <li><a href="#">Footer link</a></li>
        <li><a href="#">Footer link</a></li>
        <li><a href="#">Footer link</a></li>
      </ul>
      <ul class="column">
        <li><a href="#">Footer link</a></li>
        <li><a href="#">Footer link</a></li>
        <li><a href="#">Footer link</a></li>
        <li><a href="#">Footer link</a></li>
        <li><a href="#">Footer link</a></li>
      </ul>
    </div>
  </footer>
</template>

<script>

export default {
  name: 'Footer',
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

.footer {
  padding: 15em 0;
  display: flex;
  justify-content: center;
  align-items: center;
  background: rgba(47, 54, 64,1.0);
  background-repeat: repeat;
  background-image: 
    linear-gradient(
      to right bottom, rgba(23, 27, 32, 0.45), rgba(47, 54, 64, 0.65)),
      url(../assets/images/textures/cartographer.png);

  &__content {
    width: 100%;
    padding: 0 5%;
    max-width: 1440px;
    display: flex;
    justify-content: flex-start;
  }

  .column {
    display: flex;
    flex-direction: column;
    width: 33.33%;
    list-style-type: none;
    padding: 0;
    margin: 0;

    li {
      margin: 8px 0;
      font-size: 18px;
    }

    li > a {
      color: var(--offWhite);
      text-decoration: none;
      font-weight: bold;
      text-transform: uppercase;
      letter-spacing: 2px;
    }
  }

}


</style>
