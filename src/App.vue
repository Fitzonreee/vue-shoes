<template>
  <div id="app">
    <Navbar />
    <Cart />
    <Hero />
    <ProductGallery />
    <Newsletter />
    <PhotoGallery />
    <Footer />
  </div>
</template>

<script>

import Navbar from './components/Navbar.vue'
import Cart from './components/Cart.vue'
import Hero from './components/Hero.vue'
import ProductGallery from './components/ProductGallery.vue'
import Newsletter from './components/Newsletter.vue'
import PhotoGallery from './components/PhotoGallery.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'app',
  components: {
    Navbar,
    Cart,
    Hero,
    ProductGallery,
    Newsletter,
    PhotoGallery,
    Footer
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  position: relative;
}

html,
body {
  margin: 0;
  padding: 0;
}
</style>
