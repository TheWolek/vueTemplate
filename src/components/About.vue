<template>
  <div class="container" id="about">
    <section class="card">
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
    <section class="card">
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
  background: lightgray;
  padding: 10em 1em 5em 1em;
  display: grid;
  place-items: center;
  gap: 3em;

  .card {
    width: 100%;
    display: grid;
    place-items: center;
    gap: 0.5em;
    background: #e5c06d;
    border-radius: 3px;
    padding: 0.7em;

    img {
      max-width: 90%;
      border-radius: 5px;
    }

    .card-text {
      width: 100%;
      padding: 0.5em;
    }
  }
}

@media screen and (min-width: 768px) {
  .container {
    .card {
      padding-top: 2em;
      padding-bottom: 1.5em;
      img {
        max-width: 80%;
      }

      .card-text {
        max-width: 90%;
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
