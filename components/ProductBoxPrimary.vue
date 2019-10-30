<template>
  <div class="col">
    <div class="product-box product-box--primary" data-tile-id="Product Box Primary" nav-tile="true">
      <!-- <div class="product-box__content">
        <div class="title">THE<br>DOLLAR<br>EVENT</div>
        <p>Look for new prices all over the store.</p>
        <a class="subtitle"><span>{{ date }}</span></a>
      </div> -->
    </div>
  </div>
</template>

<script>
export default {
  props: {
    date: {
      type: String,
      default: null
    },
  }
}
</script>

<style lang="scss" scoped>
.product-box--primary {
  background: $white url('/images/primary.png');
  background-size: cover;
  // background: $dark-orange;
  color: $white;
  cursor: pointer;

  .product-box__content {
    margin-top: 5%;
    flex-wrap: wrap;
    position: static;
    text-align: center;
    justify-content: center;
    font-family: 'Sharp Grotesk';
  }

  .title {
    color: transparent;
    font: 800 12vw 'Sharp Grotesk';
    -webkit-text-stroke: 1px $red;
    text-shadow: -2px -1px 0 $white;

    @media screen and (min-width: $tablet) {
      font-size: 34px;
    }
  }

  p {
    font-weight: 100;
    line-height: 18px;
    margin: 10px 0;
  }

  .subtitle {
    background: $red;
    padding: 15px 0;
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    width: 100%;
    font-weight: 500;
    font-size: 14px;
    line-height: 17px;

    span {
      border: 1px solid;
      padding: 20px 10px 10px;
      position: relative;
      top: -2px;
    }
  }
}
</style>
