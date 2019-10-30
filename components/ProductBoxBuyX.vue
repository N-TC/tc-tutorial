<template>
  <div class="product-box product-box--buy-x-get promotion" data-tile-id="Buy X Promotion">

    <div class="column">
      {{ product.description }}
    </div>

    <div class="column">
      right
    </div>


    <img
      class="product-box__image"
      :src="'https://tcdigitanewtest.azurewebsites.net/flyers/2019/36/LA-L1/' + product.promoImage"
    >


    <!-- <div class="content">
      <div class="title">Buy 1</div>
      <div class="wpr">
        <div class="text">Brita water bottle</div>
        <div class="subtext">Save $5 19.99 ea</div>
        <div class="code">21012470001/21163994</div>
      </div>

      <div class="image-wpr">
        <div class="product-box__image-wpr">
          <img class="product-box__image lazy" src="bottle.png" alt="">
        </div>
      </div>
    </div>

    <div class="content">
      <div class="title">Get 1 free</div>
      <div class="wpr">
        <div class="text">Brita filter 2 pack</div>
        <div class="code">21012470001/21163994</div>
      </div>

      <div class="image-wpr">
        <div class="product-box__image-wpr">
          <img class="product-box__image lazy" src="filter.png" alt="">
      </div>
    </div>
    </div> -->
  </div>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      default: null
    },
    date: {
      type: String,
      default: null
    }
  },

  mounted() {
    console.log('Buy X', this.product)
  }
}
</script>

<style lang="scss" scoped>
.product-box--buy-x-get {
  flex-direction: row;
  justify-content: space-around;

  .column {
    border: 1px solid lime;
    flex: 1;
  }

  .product-box__image {
    bottom: 10px;
    height: 50%;
  }
}
</style>
