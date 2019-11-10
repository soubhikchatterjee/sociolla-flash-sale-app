<template>
  <div class="timer-wrapper">
    <div class="content">Berakhir Dalam</div>
    <div class="timers">
      <Time :time="6" />
      <span class="seperator">:</span>
      <Time :time="36" />
      <span class="seperator">:</span>
      <Time :time="20" />
    </div>
  </div>
</template>

<script>
import Time from "./Time";
export default {
  name: "Timer",
  components: {
    Time
  }
};
</script>

<style lang="scss">
@import "@/scss/_variables.scss";
.timer-wrapper {
  display: flex;
  align-items: center;
  .content {
    margin-right: 15px;
    text-transform: uppercase;
    font-size: 0.77rem;
    letter-spacing: 2px;
  }
  .timers {
    .seperator {
      font-size: 0.77rem;
      margin: 0 4px;
    }
  }
}
</style>