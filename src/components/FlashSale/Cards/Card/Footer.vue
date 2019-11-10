<template>
  <div class="footer">
    <div class="progress-bar-wrapper" v-if="showProgress === true">
      <div class="progress-bar-background-hot">
        <div class="progress-bar-foreground">
          <div :class="'progress-percentage-' + progressPercentage"></div>
        </div>
      </div>
      <div v-if="!isPopular" :class="'progress-bar-label-' + popularity">Sudah terjual 15</div>
      <div v-if="isPopular" :class="'progress-bar-label-' + popularity">Segera habis</div>
    </div>
    <a href="#" class="btn-review" v-if="type !== 'soldout' && !showProgress">See Review</a>
    <div class="label-sold" v-if="type==='soldout'">Tersedia dalam harga normal</div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  props: ["type", "showProgress", "progressPercentage"],
  computed: {
    popularity() {
      return this.isPopular ? "hot" : "cold";
    },
    isPopular() {
      return this.progressPercentage > 50;
    }
  }
};
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

.footer {
  a.btn-review {
    border: 1px solid #000000;
    color: #000000;
    padding: 4px;
    font-size: 0.64rem;
    letter-spacing: 1px;
    font-weight: bold;
    text-transform: uppercase;
    border-radius: 4px;
    text-decoration: none;
    width: 100%;
    text-align: center;
    display: inline-block;

    &:hover {
      border: 1px solid $primary-color;
      color: $primary-color;
    }
  }
  .progress-bar-wrapper {
    .progress-bar-background-hot {
      background: $progress-bar-bg-hot;
      width: 100%;
      height: 8px;
      border-radius: 8px;

      .progress-bar-foreground {
        height: 8px;
        width: 100%;
        border-radius: 8px;
        height: 8px;

        .progress-percentage-30 {
          @extend .progress-bar-foreground;
          background: $primary-color;
          width: 30%;
        }
        .progress-percentage-80 {
          @extend .progress-bar-foreground;
          background: $primary-color;
          width: 80%;
        }
      }
    }

    .progress-bar-label-hot {
      color: $primary-color;
      font-size: 0.69rem;
      text-transform: uppercase;
      margin-top: 5px;
      letter-spacing: 1px;
    }
    .progress-bar-label-cold {
      color: #cccccc;
      font-size: 0.69rem;
      margin-top: 5px;
    }
  }
  .label-sold {
    font-size: 0.57rem;
    color: $primary-color;
    text-align: center;
  }
}
</style>