<template>
  <div class="header">
    <div class="no-discount" v-if="type==='soldout'"></div>
    <div class="discount" v-else>34%</div>
    <div class="favourite">
      <i class="far fa-star"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: ["type"]
};
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

.header {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-bottom: 15px;
  .discount {
    background: $primary-color;
    border-radius: 50%;
    padding: 5px;
    height: 25px;
    width: 25px;
    color: #ffffff;
    font-size: 0.55rem;
    line-height: 15px;
  }
  .favourite {
    color: #cccccc;
    cursor: pointer;
  }
}
</style>