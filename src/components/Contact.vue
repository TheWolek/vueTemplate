<template>
  <section class="container" id="contact">
    <div class="mapContainer">
      <iframe
        width="600"
        style="border:0"
        loading="lazy"
        src="https://www.google.com/maps/embed/v1/place?q=place_id:ChIJgQYZJXe2EEcREHmn1biW3Qw&zoom=14&key=AIzaSyA9DxaysegfoYFJUGnZixWWE09_L-7wg_0"
      ></iframe>
    </div>
    <div class="textContainer">
      <address>
        <p>Remont</p>
        <p>Krótka 12</p>
        <p>42-202 Częstochowa</p>
        <p>Tel. 696911299</p>
        <p>mail@example.com</p>
      </address>
    </div>
  </section>
</template>
<script>
export default {
  name: "contact",
};
</script>
<style lang="scss" scoped>
.container {
  width: 100%;
  height: 650px;
  background: lightblue;
  padding: 5em 1em 2em 1em;
  display: grid;
  grid-template-rows: 3fr 2fr;
  gap: 1em;

  .mapContainer {
    width: 100%;
    // height: 65vh;

    iframe {
      width: 100%;
      height: 100%;
    }
  }

  .textContainer {
    address {
      p {
        font-style: normal;
        font-size: 1.2rem;
      }
      p + p {
        margin-top: 0.2em;
      }
    }
  }
}

@media screen and (min-width: 768px) {
  .container {
    padding: 8em 1.2em 2em 1.2em;
  }

  address {
    font-size: 105%;
    p {
      font-size: 132%;
    }
  }
}

@media screen and (min-width: 1024px) {
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-bottom: 4em;

    .mapContainer {
      width: 50%;
      order: 2;
      box-shadow: 2px 5px 9px 1px rgba(0, 0, 0, 0.64);
    }

    .textContainer {
      width: 20%;
      height: 65vh;
      display: flex;
      align-items: center;
      background: rgba(0, 0, 0, 0.4);
      color: rgb(243, 243, 243);
      order: 1;
      text-align: left;
      font-size: 100%;
      padding-left: 2em;
      border-top-left-radius: 25px;
      border-bottom-left-radius: 25px;
      box-shadow: -1px 5px 9px 1px rgba(0, 0, 0, 0.64);
    }
  }
}
</style>
