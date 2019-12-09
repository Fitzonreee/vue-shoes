<template>
  <nav class="nav">
    <ul>
      <li class="logo">
        <a href="/"><img src="../assets/images/icons/acme_logo.png" alt="Logo"></a>
      </li>
      <li class="bag" @click="toggleClass()">
        <div class="bag__count">{{ count }}</div>
        <img src="../assets/images/icons/bag.png" alt="Shopping bag">
      </li>
    </ul>
  </nav>
</template>

<script>

export default {
  name: 'Navbar',
  props: {
    msg: String
  },
  data() {
    return {
      count: 3
    }
  },
  methods: {
    toggleClass: function() {
      document.getElementsByTagName('body')[0].classList.add('active')
    }
  },

}
</script>

<style lang="scss" scoped>

.nav {
  padding: 0.65em;
  box-shadow: 0px 3px 15px rgba(0,0,0,0.15);
  // position: fixed;
  // z-index: 30;
  // background: $white;
}

ul {
  list-style-type: none;
  padding: 0;
  margin: 0 auto;
  width: 90%;
  max-width: 1440px;
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

.logo {
  margin-right: auto;

  img {
    width: 100px;
  }

  a {
    display: flex;
    justify-content: center;
    align-items: center
  }
}

.bag {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  position: relative;

  &__count {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    top: 13px;
    background: #c23616;
    color: var(--offWhite);
    border-radius: 100%;
    font-size: 11px;
    width: 15px;
    height: 15px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  img {
    width: 30px;
    &:hover {
      cursor: pointer;
    }
  }
}

</style>
