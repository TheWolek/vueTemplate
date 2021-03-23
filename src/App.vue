<template>
  <div id="app">
    <div id="nav">
      <a href="#">Home</a>
      <a href="#">About</a>
      <a href="#">Contact</a>
    </div>
    <div class="nav-bar-mobile">
      <img src="./assets/logo.png" />
      <div id="hamburger" @click="ToggleNav">
        <span id="1"></span>
        <span id="2"></span>
        <span id="3"></span>
      </div>
    </div>
    <div id="nav-mobile">
      <a href="#">Home</a>
      <a href="#">About</a>
      <a href="#">Contact</a>
    </div>
    <Landing></Landing>
  </div>
</template>

<script>
//import HelloWorld from "./components/HelloWorld.vue";
import Landing from "./components/Landing.vue";

export default {
  name: "App",
  components: {
    Landing,
  },
  methods: {
    ToggleNav: function() {
      document
        .getElementById("nav-mobile")
        .classList.toggle("nav-mobile-active");

      document.getElementById("1").classList.toggle("ham-1");
      document.getElementById("2").classList.toggle("ham-2");
      document.getElementById("3").classList.toggle("ham-3");
    },
  },
};
</script>

<style lang="scss">
$font-dark: #2c3e50;

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  position: relative;
  overflow-x: hidden;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: $font-dark;
}

#nav-mobile {
  position: absolute;
  top: -200px;
  left: 0;
  width: 100%;
  z-index: 99;
  display: flex;
  flex-direction: column;
  justify-content: center;
  border-bottom: 2px solid $font-dark;
  border-top: 2px solid $font-dark;
  background: #f8f8f8;
  transition: all 0.7s ease-in-out;

  a {
    padding: 20px;
    font-weight: bold;
    color: $font-dark;

    // &.router-link-exact-active {
    //   color: #42b983;
    // }
  }

  a + a {
    border-top: 1px solid $font-dark;
  }
}

.nav-mobile-active {
  transform: translateY(calc(200px + 7vh));
}

.nav-bar-mobile {
  position: relative;
  padding: 0 0.5em;
  width: 100%;
  height: 8vh;
  z-index: 100;
  background: white;
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 2px solid $font-dark;

  #hamburger {
    width: 40px;
    height: 40px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;

    &:hover {
      cursor: pointer;
    }

    span {
      display: block;
      width: 100%;
      height: 6px;
      border-radius: 2px;
      background: $font-dark;
      transition: all 0.3s ease;
    }
  }

  img {
    height: 95%;
  }
}

.ham-1 {
  transform: rotate(45deg) translate(9px, 9px);
}

.ham-2 {
  opacity: 0;
}

.ham-3 {
  transform: rotate(-45deg) translate(10px, -10px);
}

#nav {
  display: none;
  padding: 30px;

  a {
    font-weight: bold;
    color: $font-dark;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
