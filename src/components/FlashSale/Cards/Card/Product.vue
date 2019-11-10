<template>
  <div class="product-image">
    <div class="sold-out-wrapper" v-if="type==='soldout'">
      <div class="sold-out-content">
        <div class="text">FlashSale Sold Out</div>
      </div>
    </div>
    <img src="@/assets/product.jpg" />
  </div>
</template>

<script>
export default {
  name: "Product",
  props: ["type"]
};
</script>

<style lang="scss" scoped>
.product-image {
  position: relative;
  img {
    width: 100%;
    height: 100px;
  }
  margin-bottom: 15px;
  .sold-out-wrapper {
    position: absolute;
    width: 100%;
    height: 100%;
    background: rgba(255, 252, 252, 0.7);

    .sold-out-content {
      width: 100%;
      height: 100%;
      margin: auto;
      display: flex;
      justify-content: center;
      align-items: center;
      .text {
        background: rgba(0, 0, 0, 0.3);
        padding: 13px;
        color: #ffffff;
        text-transform: uppercase;
        font-size: 0.56rem;
        letter-spacing: 1px;
      }
    }
  }
}
</style>