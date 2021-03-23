<template>
  <div class="container" id="contact">
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
  </div>
</template>
<script>
export default {
  name: "contact",
};
</script>
<style lang="scss" scoped>
.container {
  width: 100%;
  background: lightblue;
  padding: 5em 1em 2em 1em;

  .mapContainer {
    width: 100%;
    height: 65vh;

    iframe {
      width: 100%;
      height: 100%;
    }
  }
}

address {
  padding-top: 1em;
  p {
    font-style: normal;
    font-size: 1.2rem;
  }
  p + p {
    margin-top: 0.2em;
  }
}
</style>
