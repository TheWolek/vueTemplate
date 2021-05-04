<template>
  <div
    class="container col-12 col-sm-12 col-md-12 col-lg-10 col-xl-10"
    id="about"
  >
    <section class="card">
      <div class="card-img">
        <img
          src="https://www.kobieta.pl/media/cache/default_view/uploads/media/default/0003/20/remont-mieszkania.jpeg"
        />
      </div>
      <div class="card-text">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quibusdam at
        assumenda modi fugiat nobis iste inventore possimus consequatur illo
        quis cum quos incidunt corrupti pariatur, temporibus sunt odio excepturi
        alias!
      </div>
    </section>
    <section class="card">
      <div class="card-img">
        <img
          src="https://www.kobieta.pl/media/cache/default_view/uploads/media/default/0003/20/remont-mieszkania.jpeg"
        />
      </div>
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
@import "/styles/common.scss";

.container {
  // background: $bg-light;
  padding: 10em 0.7em;
  display: grid;
  place-items: center;
  gap: 3em;

  .card {
    display: grid;
    place-items: center;
    gap: 0.5em;
    background: $bg-yellow;
    border-radius: 3px;
    padding: 0.7em;

    .card-img {
      max-width: 90%;
      border-radius: 5px;

      img {
        max-width: 100%;
        max-height: 100%;
      }
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

      .card-img {
        max-width: 80%;

        img {
          max-width: 100%;
          max-height: 100%;
        }
      }

      .card-text {
        max-width: 90%;
        font-size: 1.22rem;
      }
    }
  }
}

@media screen and (min-width: 1024px) {
  .container {
    grid-template-columns: 8% [left] 1fr [right] 1fr 8%;
    gap: 0;
    padding-bottom: 13em;
    padding-top: 13em;
    .card {
      width: 70%;
      grid-column: left;

      &:nth-child(2) {
        grid-column: right;
      }

      .card-img {
        max-width: 85%;
        overflow: hidden;

        img {
          max-width: 100%;
          max-height: 100%;
          transition: all 0.3s ease-in-out;

          &:hover {
            transform: scale(1.1);
          }
        }
      }
    }
  }
}
</style>
