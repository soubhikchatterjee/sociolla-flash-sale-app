<template>
  <span class="time">{{time}}</span>
</template>

<script>
export default {
  name: "Time",
  props: ["time"]
};
</script>

<style lang="scss">
@import "@/scss/_variables.scss";
.time {
  background-color: $timer-bg-color;
  padding: 5px;
  border-radius: 2px;
  font-size: 0.55rem;
}
</style>