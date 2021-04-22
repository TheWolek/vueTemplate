<template>
  <section class="container col-12" id="contact">
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
  height: 650px;
  background: lightblue;
  padding: 5em 1em 2em 1em;
  display: grid;
  grid-template-rows: 3fr 2fr;
  gap: 1em;

  .mapContainer {
    width: 100%;

    iframe {
      width: 100%;
      height: 100%;
    }
  }

  .textContainer {
    address {
      p {
        font-style: normal;
        font-size: 1.15rem;
        margin-bottom: 0;
      }
      p + p {
        margin-top: 0.2em;
      }
    }
  }
}

@media screen and (min-width: 768px) {
  .container {
    grid-template-columns: 4% [center] 1fr 4%;
    gap: 0;
    row-gap: 1em;

    .mapContainer {
      grid-column: center;
      grid-row: 1;
    }

    .textContainer {
      grid-column: center;
      grid-row: 2;
    }
  }
}

@media screen and (min-width: 1024px) {
  .container {
    grid-template-rows: 1fr;
    grid-template-columns: 7% [left] 1fr [right] 4fr 10%;
    gap: 0;
    // column-gap: 1em;
    padding: 3em 2rem;
    .mapContainer {
      grid-column: right;
      grid-row: 1;
      padding: 1em;
    }

    .textContainer {
      grid-column: left;
      grid-row: 1;
      display: grid;
      justify-items: right;
      align-content: center;
      padding-right: 1em;
      // box-shadow: -1px 5px 9px 1px rgba(0, 0, 0, 0.64);

      address {
        text-align: right;
        font-weight: bold;
      }
    }
  }
}
</style>
