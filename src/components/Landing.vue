<template>
  <div
    class="container col-12 col-sm-12 col-md-12 col-lg-12 col-xl-12"
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
  // height: 80vh;
  background: $bg-light;
  display: flex;
  justify-content: center;
  align-items: center;
  color: $font-light;
  // background-image: url("https://alebank.pl/wp-content/uploads/2019/10/remont-mieszkanie-malowanie.jpg");
  background-image: linear-gradient(
      180deg,
      rgba(0, 0, 0, 0.43) 0%,
      rgba(0, 0, 0, 0.43) 100%
    ),
    url(https://budmardesign.pl/wp-content/uploads/2019/09/interior-design-35.jpg) !important;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  padding: 60% 0;

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
    padding: 50% 0;
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
    // background-position-y: center;
    background-size: cover;
    // background-attachment: fixed;
    padding: 17% 0;
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
