<template>
  <div class="container" id="about">
    <div class="card">
      <div class="card-img"></div>
      <div class="card-text">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quibusdam at
        assumenda modi fugiat nobis iste inventore possimus consequatur illo
        quis cum quos incidunt corrupti pariatur, temporibus sunt odio excepturi
        alias!
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "about",
};
</script>
<style lang="scss" scoped>
.container {
  width: 100%;
  height: 100vh;
  background: lightgray;
  padding: 5em 1em 1em 1em;

  .card {
    width: 100%;
    height: 500px;

    .card-img {
      width: 90%;
      height: 50%;
      margin: 0 auto;
      background-image: url("https://www.kobieta.pl/media/cache/default_view/uploads/media/default/0003/20/remont-mieszkania.jpeg");
      background-size: 100%;
      background-repeat: no-repeat;
    }

    .card-txt {
      width: 100%;
      background: rgba(0, 0, 0, 0.1);
    }
  }
}
</style>
