<template>
    <aside class="cart">
      <div class="close" @click="closeCart()">
        <svg class="close__icon" viewPort="0 0 20 20" version="1.1"
            xmlns="http://www.w3.org/2000/svg">
            <line x1="1" y1="18" 
                  x2="18" y2="1" 
                  stroke="black" 
                  stroke-width="2"/>
            <line x1="1" y1="1" 
                  x2="18" y2="18" 
                  stroke="black" 
                  stroke-width="2"/>
        </svg>
      </div>

      <ul class="cart__items">
        <li class="item" v-for="product in products" :key="product.index">
          <img class="item__image" :src="getImageURL(product.src)" alt="Vans placeholder">
          <div class="item__details">
            <h6 class="item__brand">{{product.brand}}</h6>
            <h3 class="item__model">{{product.model}}</h3>
          </div>
          <p class="item__price">{{ `$${product.price}` }}</p>
        </li>
      </ul>
       
    </aside>
</template>

<script>
import productData from '../assets/data/products.js'

export default {
  name: 'Cart',
  props: {
    msg: String
  },
  data() {
    return {
      products: productData
    }
  },
  methods: {
    closeCart: function() {
      document.getElementsByTagName('body')[0].classList.remove('active')
    },
    getImageURL: function(src) {
      var images = require.context('../assets/images/products/', false, /\.png$/)
      return images('./' + src + ".png")
    }
  }
}
</script>

<style lang="scss" scoped>

.cart {
  margin: 0;
  padding: 0;
  background: var(--offWhite);
  box-shadow: 0px 3px 15px rgba(0,0,0,0.15);
  position: fixed;
  top: 0;
  right: 0;
  width: 400px;
  height: 100vh;
  overflow-y: scroll;
  transition: all 300ms cubic-bezier(.42,0,.58,1);
  transform: translateX(400px);
  z-index: 999;

  &__items {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    padding: 0 2em;
    margin: 0;
  }
}

.close {
  margin: 22px 0 0 20px;
  display: inline-block;
  cursor: pointer;
  &__icon {
    width: 26px;
    height: 26px;
  }
}

.item {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  width: 100%;
  margin: 12px 0;

  &__image {
    max-width: 80px;
    margin-right: 26px;
  }

  &__details {
    margin-right: auto;
  }

  &__brand {
    margin: 0;
  }

  &__model {
    margin: 0;
  }

}

</style>