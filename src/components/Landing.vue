<template>
  <div class="container" id="landing">
    <header>
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
.container {
  // width: 100%;
  height: 80vh;
  background: lightgray;
  display: flex;
  justify-content: center;
  align-items: center;
  color: rgb(180, 180, 180);
  background-image: url("https://alebank.pl/wp-content/uploads/2019/10/remont-mieszkanie-malowanie.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position-x: 65%;
  padding: 0;

  header {
    color: white;
    width: 100%;
    padding: 0.7em;
    background: rgba(0, 0, 0, 0.4);

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

@media screen and (min-width: 768px) {
  .wrap {
    header {
      h1 {
        font-size: 3rem;
      }

      h4 {
        font-size: 1.2rem;
      }

      h1 + * {
        margin-top: 0.5em;
      }
    }
  }
}

@media screen and (min-width: 1024px) {
  .wrap {
    background-position-y: 50%;
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
