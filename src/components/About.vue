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
    grid-template-columns: 5% [center] 1fr [center_end] 5%;
    .card {
      padding-top: 2em;
      padding-bottom: 1.5em;
      grid-column: center;

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
    grid-template-columns: 8% [left] 1fr [right] 1fr 8%;
    gap: 0;
    padding-bottom: 9em;
    .card {
      width: 90%;
      grid-column: left;

      &:nth-child(2) {
        grid-column: right;
      }

      img {
        max-width: 85%;
      }
      .card-text {
      }
    }
  }
}
</style>
