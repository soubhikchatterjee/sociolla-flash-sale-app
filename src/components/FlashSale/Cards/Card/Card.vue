<template>
  <div class="card">
    <Header :type="type" />
    <Product :type="type" />
    <ProductInfo
      :type="type"
      :more-options="moreOptions"
      :title="title"
      :description="description"
      :oldPrice="oldPrice"
      :newPrice="newPrice"
    />
    <Footer
      :type="type"
      :showProgress="showProgress"
      :progress-percentage="progressPercentage"
    />
  </div>
</template>

<script>
import Header from "./Header";
import Product from "./Product";
import ProductInfo from "./ProductInfo";
import Footer from "./Footer";

export default {
  name: "Card",
  components: {
    Header,
    Product,
    ProductInfo,
    Footer
  },
  props: [
    "type",
    "moreOptions",
    "title",
    "description",
    "oldPrice",
    "newPrice",
    "showProgress",
    "progressPercentage"
  ],
  created() {
    // console.log("created", this.showProgress);
  }
};
</script>


<style lang="scss" scoped>
@import "@/scss/_variables.scss";

.card {
  background: #ffffff;
  min-height: 350px;
  max-height: 350px;
  width: 200px;
  height: 100%;
  padding: 8px;
  margin-left: 10px;
  margin-right: 10px;
  display: flex;
  flex-direction: column;
}
</style>