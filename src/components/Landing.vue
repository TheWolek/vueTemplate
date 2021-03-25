<template>
  <div class="wrap">
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
.wrap {
  width: 100%;
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
  }
}
</style>
