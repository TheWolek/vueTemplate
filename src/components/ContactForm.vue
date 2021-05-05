<template>
  <div class="container">
    <h1>Skontaktuj się z nami:</h1>
    <form action="#">
      <div class="form-section">
        <label for="mail">e-mail</label>
        <input type="email" name="mail" id="mail" />
      </div>
      <div class="form-section">
        <label for="name">Imie i Nazwisko</label>
        <input type="text" name="name" id="name" />
      </div>
      <div class="form-section">
        <label for="phone">nr. telefonu</label>
        <input type="tel" name="phone" id="phone" />
      </div>
      <div class="form-section">
        <label for="message">wiadomość</label>
        <textarea name="message" id="message" cols="30" rows="10"></textarea>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "contactForm",
};
</script>

<style lang="scss" scoped>
@import "/styles/common.scss";

.container {
  h1 {
    font-size: clamp(1.2rem, 5vw, 2rem);
    margin-bottom: 0.7em;
  }

  form {
    display: grid;

    .form-section {
      label {
        position: absolute;
      }

      input,
      textarea {
        outline: none;
        border: none;
        border-bottom: 1px solid $font-dark;
      }

      textarea {
        resize: none;
      }
    }
  }
}
</style>
