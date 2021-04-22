<template>
  <footer>
    <div class="content">
      <p>Remont</p>
      <p>© Paweł Michalski</p>
    </div>
  </footer>
</template>
<script>
export default {
  name: "footer",
};
</script>
<style lang="scss" scoped>
footer {
  width: 100%;
  padding: 0.7em;
  background: rgb(50, 115, 145);
  color: black;

  p {
    margin: 0;
  }
}

@media screen and (min-width: 768px) {
  footer {
    font-size: 110%;
  }
}
</style>
