<template>
  <div class="app">

    <h3 class="headline">New Arrivals</h3>

    <ul class="products">
      <li class="products__item" v-for="product in products" :key="product.index">

        <div class="item__image" :style="{ 'background-image': `linear-gradient(to right, ${product.colorStart}, ${product.colorEnd}}` }">
          <img src="../assets/images/products/vans-placeholder.png" alt="Product image" />
        </div>
        
        <div class="item__details">
          <div class="details">
            <h2 class="item__brand">{{ product.brand }}</h2>
            <h1 class="item__model">{{ product.model }}</h1>
            <h3 class="item__price">{{ `$${product.price}` }}</h3>
          </div>
          <div class="actions">
            <select class="sizes">
              <option class="sizes__option" value="" v-for="size in product.sizes" :key="size.index">{{size}}</option>
            </select>
            <button class="item__add" @click="addToCart()">
              <span>+</span>
            </button>
          </div>
        </div>

      </li>
    </ul>
    
  </div>
</template>

<script>

import productData from '../assets/data/products.js'

export default {
  props: {
    msg: String
  },
  methods: {
    addToCart: function() {
      alert("Add to cart")
    }
  }, 
  data() {
    return {
        products: productData
    }
  }
}
</script>

<style lang="scss" scoped>

.headline {
  text-align: center;
  font-size: 1.85em;
  color: rgba(47, 54, 64,0.90);
  letter-spacing: 1px;
  padding: 1.25em 0 0.25em 0;
  position: relative;

  &::after {
    content: " ";
    position: absolute;
    width: 50px;
    height: 4px;
    background: #c23616;
    margin-top: 55px;
    left: 50%;
    transform: translateX(-50%);
  }
}

.products {
  padding: 0 0 220px 0;
  margin: 80px auto 0;
  list-style-type: none;
  width: 90%;
  max-width: 1440px;
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  grid-column-gap: 26px;
  grid-row-gap: 40px;

  @media screen and (min-width: 40em) {
    grid-template-columns: repeat(2, 1fr);
  }

  @media screen and (min-width: 64em) {
    grid-template-columns: repeat(3, 1fr);
  }

  @media screen and (min-width: 75em) {
    grid-template-columns: repeat(4, 1fr);
    grid-row-gap: 60px;
  }

}

  .item {

    &__details {
      display: flex;

      .details {
        margin-right: auto;
      }

      .actions {
        display: flex;
        margin-top: auto;
      }

      .sizes {
        appearance: none;
        outline: 0;
        box-shadow: none;
        background: transparent;
        border: 1px solid rgba(194, 54, 22,1.0);
        color: rgba(194, 54, 22,1.0);
        background: transparent;
        background-image: none;
        border-radius: 30px 0 0 30px;
        padding: 0.35em 0.65em;
        text-align-last: center;
      }


    }

    &__add {
      border-radius: 0 30px 30px 0;
      padding: 0.35em 0.85em 0.35em 0.65em;
      font-size: 0.95em;
      border: 1px solid rgba(194, 54, 22,1.0);
      border-left: none;
      color: rgba(194, 54, 22,1.0);
      box-sizing: border-box;
      display: flex;
      align-items: center;

      span { margin-top: -3px; }
    }



    &__brand {
      font-size: 10px;
      margin: 10px 0 1px 0;
      text-transform: uppercase;
      letter-spacing: 2px;
      color: rgba(53, 59, 72, 0.65);
    }

    &__model {
      margin: 0;
      font-size: 1.1em;
      color: rgba(47, 54, 64,1.0);
    }

    &__price {
      margin: 5px 0 0 0;
      color: rgba(194, 54, 22,1.0);
      font-weight: 400;
      letter-spacing: 1px;
    }


    &__image {
      background: rgba(0, 0, 0, 0.05);
      height: 16em;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      &:hover img {
        transform: scale(1.125)
      }

      img {
        max-width: 65%;
        transition: all 200ms ease;
      }
    }
  }



</style>
