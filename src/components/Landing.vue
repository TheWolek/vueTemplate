<template>
  <div
    class="container col-12 col-sm-12 col-md-12 col-lg-10 col-xl-10"
    id="landing"
  >
    <header class="col-12 col-sm-12 col-md-12 col-lg-12 col-xl-12">
      <h1>Remont?</h1>
      <h4>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium
        reprehenderit veritatis consectetur
      </h4>
    </header>
  </div>
</template>
<script>
export default {
  name: "landing",
};
</script>
<style lang="scss" scoped>
@import "/styles/common.scss";

.container {
  // width: 100%;
  height: 80vh;
  background: $bg-light;
  display: flex;
  justify-content: center;
  align-items: center;
  // color: rgb(180, 180, 180);
  color: $font-light;
  background-image: url("https://alebank.pl/wp-content/uploads/2019/10/remont-mieszkanie-malowanie.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position-x: 65%;
  padding: 0;

  header {
    color: $font-light;
    // width: 100%;
    padding: 0.7em;
    background: $bg-blackGlass;

    h1 {
      font-size: 2.3rem;
    }
    h1 + * {
      margin-top: 0.4em;
    }

    h4 {
      font-size: 1.2rem;
    }
  }
}

@media (min-width: 768px) {
  .container {
    header {
      padding: 3em;
      h1 {
        font-size: 3rem;
      }

      h4 {
        font-size: 1.4rem;
      }

      h1 + * {
        margin-top: 0.5em;
      }
    }
  }
}

@media screen and (min-width: 1024px) {
  .container {
    background-position-y: center;
    background-size: contain;
    background-attachment: fixed;
    header {
      display: flex;
      flex-direction: column;
      justify-content: center;
      min-height: 20vh;

      h1 + * {
        margin-top: 1em;
      }
    }
  }
}
</style>
