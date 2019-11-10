<template>
  <div class="cards-wrapper">
    <div class="card-navigate-arrow">
      <i class="fas fa-chevron-left"></i>
    </div>
    <!-- Card -->
    <Card
      title="LANEIGE"
      description="Cushion Duo Set 1"
      old-price="1,500.000"
      new-price="1,148.000"
      :more-options="false"
      :show-progress="false"
      :progress-percentage="0"
    />
    <Card
      title="MASAMI SOUKO PROFESSIONAL"
      description="Cushion Duo Set 2"
      old-price="1,500.000"
      new-price="1,148.000"
      :more-options="true"
      :show-progress="true"
      :progress-percentage="80"
    />
    <Card
      title="MASAMI SOUKO PROFESSIONAL"
      description="Cushion Duo Set 3"
      old-price="1,500.000"
      new-price="1,148.000"
      :more-options="true"
      :show-progress="true"
      :progress-percentage="30"
    />
    <!-- Soldout -->
    <Card
      title="MASAMI SOUKO PROFESSIONAL"
      description="Cushion Duo Set 4"
      old-price="1,500.000"
      new-price="1,148.000"
      type="soldout"
      :more-options="false"
      :show-progress="false"
      :progress-percentage="0"
    />
    <Card
      title="MASAMI SOUKO"
      description="Cushion Duo Set 5"
      old-price="1,500.000"
      new-price="1,148.000"
      :more-options="true"
      :show-progress="true"
      :progress-percentage="30"
    />

    <div class="card-navigate-arrow">
      <i class="fas fa-chevron-right"></i>
    </div>
  </div>
</template>

<script>
import Card from "./Card/Card";
export default {
  name: "Cards",
  components: { Card }
};
</script>

<style lang="scss" scoped>
.cards-wrapper {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-top: 40px;
  height: 350px;
}
</style>