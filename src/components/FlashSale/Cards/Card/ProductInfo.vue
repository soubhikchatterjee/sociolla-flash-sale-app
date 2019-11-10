<template>
  <div :class="classObject">
    <h2 class="product-title">{{title}}</h2>
    <p class="content">{{description}}</p>
    <div class="old-price">Rp {{oldPrice}}</div>
    <div class="new-price">Rp {{newPrice}}</div>
    <div
      href="#"
      class="more-options"
      v-if="type==='soldout' && moreOptions === false"
    >(Flash Sale Price)</div>
    <a href="#" class="more-options" v-if="moreOptions === true">More Options</a>
  </div>
</template>

<script>
export default {
  name: "Info",
  data() {
    return {
      classObject: {
        "product-info": true,
        soldout: this.type === "soldout"
      }
    };
  },
  props: ["type", "moreOptions", "title", "description", "oldPrice", "newPrice"]
};
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
.product-info {
  flex-grow: 1;
  width: 100%;
  text-align: center;

  h2.product-title {
    font-size: 0.65rem;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 10px;
  }
  p.content {
    font-size: 0.65rem;
    margin-bottom: 10px;
  }
  .old-price {
    font-size: 0.65rem;
    text-decoration: line-through;
    color: #cccccc;
    margin-bottom: 5px;
  }
  .new-price {
    font-size: 0.65rem;
    font-weight: bold;
  }

  a.more-options {
    font-size: 0.65rem;
    color: #cccccc;
    text-decoration: none;
    &:hover {
      color: $primary-color;
    }
  }

  div.more-options {
    @extend a.more-options;
    &:hover {
      color: #cccccc;
    }
  }

  &.soldout {
    color: #cccccc;
  }
}
</style>