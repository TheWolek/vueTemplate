<template>
  <div class="wrap">
    <Card></Card>
  </div>
</template>
<script>
import Card from "./Card.vue";

export default {
  name: "Cards",
  components: {
    Card,
  },
};
</script>
<style lang="scss" scoped>
.wrap {
  width: 100%;
  height: 60vh;
  background: lightblue;
  padding: 1em;
  display: flex;
  flex-direction: column;
  align-content: center;
}
</style>
