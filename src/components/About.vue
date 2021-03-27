<template>
  <div class="container" id="about">
    <section class="card">
      <div class="card-img"></div>
      <img
        src="https://www.kobieta.pl/media/cache/default_view/uploads/media/default/0003/20/remont-mieszkania.jpeg"
      />
      <div class="card-text">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quibusdam at
        assumenda modi fugiat nobis iste inventore possimus consequatur illo
        quis cum quos incidunt corrupti pariatur, temporibus sunt odio excepturi
        alias!
      </div>
    </section>
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

    img {
      display: none;
    }

    .card-img {
      width: 90%;
      height: 50%;
      margin: 0 auto;
      background-image: url("https://www.kobieta.pl/media/cache/default_view/uploads/media/default/0003/20/remont-mieszkania.jpeg");
      background-size: 100%;
      background-repeat: no-repeat;
    }

    .card-text {
      width: 100%;
      background: rgba(0, 0, 0, 0.1);
      padding: 0.5em;
    }
  }
}

@media screen and (min-width: 768px) {
  .container {
    font-size: 120%;
    padding-top: 10em;

    .card {
      .card-img {
        height: 100%;
      }

      .card-text {
        margin-top: 1em;
      }
    }
  }
}

@media screen and (min-width: 1024px) {
  .container {
    height: 1000px;
    display: flex;
    justify-content: center;
    .card {
      height: 100%;
      width: 70%;
      img {
        display: block;
        margin: 0 auto;
        height: 60%;
      }
      .card-img {
        display: none;
      }
      .card-text {
        width: 70%;
        margin: 1em auto;
      }
    }
  }
}
</style>
