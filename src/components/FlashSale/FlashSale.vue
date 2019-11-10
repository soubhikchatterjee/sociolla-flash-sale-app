<template>
  <div class="hero">
    <div class="container">
      <h1 class="title">Flash Sale</h1>
      <Timer />
      <Cards />

      <a href="#" class="btn-more-sale">See More</a>
    </div>
  </div>
</template>


<script>
import Timer from "./Timer";
import Cards from "./Cards/Cards";

export default {
  name: "Hero",
  components: {
    Timer,
    Cards
  }
};
</script>

<style scoped lang="scss">
@import "@/scss/_variables.scss";

.hero {
  max-width: 100vw;
  height: 600px;
  background-image: url("../../assets/hero.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;

  .container {
    margin: auto;
    max-width: 1100px;
    display: flex;
    flex-direction: column;
    align-items: center;

    h1.title {
      padding: 15px 0;
    }

    a.btn-more-sale {
      width: 150px;
      padding: 7px;
      background: #ffffff;
      border: 1px solid #000000;
      color: #000000;
      text-decoration: none;
      text-align: center;
      border-radius: 5px;
      font-size: 0.77rem;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-top: 55px;

      &:hover {
        background: $primary-color;
        border: 1px solid #000000;
        color: #ffffff;
      }
    }
  }
}
</style>