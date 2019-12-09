<template>
  <section class="gallery">
    <div class="gallery__item featured"></div>
    <div class="gallery__item gallery__item-1"></div>
    <div class="gallery__item gallery__item-2"></div>
    <div class="gallery__item gallery__item-3"></div>
    <div class="gallery__item gallery__item-4"></div>
    <div class="gallery__item gallery__item-5"></div>
    <div class="gallery__item gallery__item-6"></div>
  </section>
</template>

<script>

export default {
  name: 'PhotoGallery',
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

.gallery {
  height: 500px;

  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-template-rows: repeat(2, 1fr);

  &__item.featured {
    grid-column-start: 1;
    grid-column-end: 3; 
    grid-row-start: 1;
    grid-row-end: 3; 

    background-image: url('../assets/images/lifestyle/lifestyle-jumping.jpg');

  }

  &__item {
    display: flex;
    justify-content: center;
    align-items: center;

    background-size: cover;
    background-position: center center;

    &-1 { background-image: url('../assets/images/lifestyle/lifestyle-adidas.jpg')}
    &-2 { background-image: url('../assets/images/lifestyle/lifestyle-yeezy.jpg')}
    &-3 { background-image: url('../assets/images/lifestyle/lifestyle-black-and-white.jpg')}
    &-4 { background-image: url('../assets/images/lifestyle/lifestyle-throw.jpg')}
    &-5 { background-image: url('../assets/images/lifestyle/lifestyle-nike-air-max.jpg')}
    &-6 { background-image: url('../assets/images/lifestyle/lifestyle-adidas-walking.jpg')}
  }
}


</style>
