<template lang="pl">
  <div id="app">
    <div id="nav">
      <img src="./assets/logo.png" />
      <div class="links">
        <a href="#landing" @click="animateScroll('landing')">Home</a>
        <a href="#about" @click="animateScroll('about')">About</a>
        <a href="#contact" @click="animateScroll('contact')">Contact</a>
      </div>
    </div>
    <div class="nav-mobile-container">
      <div class="nav-bar-mobile">
        <img src="./assets/logo.png" />
        <div id="hamburger" @click="ToggleNav">
          <span id="1"></span>
          <span id="2"></span>
          <span id="3"></span>
        </div>
      </div>
      <div id="nav-mobile">
        <a href="#nav" @click="animateScroll('nav')">Home</a>
        <a href="#about" @click="animateScroll('about')">About</a>
        <a href="#contact" @click="animateScroll('contact')">Contact</a>
      </div>
    </div>
    <Landing></Landing>
    <About></About>
    <Contact></Contact>
    <Footer></Footer>
  </div>
</template>

<script>
//import HelloWorld from "./components/HelloWorld.vue";
import Landing from "./components/Landing";
import About from "./components/About";
import Contact from "./components/Contact";
import Footer from "./components/Footer";
import $ from "jquery";

export default {
  name: "App",
  components: {
    Landing,
    About,
    Contact,
    Footer,
  },
  methods: {
    ToggleNav: function() {
      $("#nav-mobile").toggleClass("nav-mobile-active");
      $("#1").toggleClass("ham-1");
      $("#2").toggleClass("ham-2");
      $("#3").toggleClass("ham-3");
    },

    animateScroll: function(el) {
      $("html, body").animate(
        {
          scrollTop: $("#" + el).offset().top,
        },
        1000
      );
      $("#nav-mobile").toggleClass("nav-mobile-active");
      $("#1").toggleClass("ham-1");
      $("#2").toggleClass("ham-2");
      $("#3").toggleClass("ham-3");
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
  // font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: $font-dark;
}

.nav-mobile-container {
  position: fixed;
  width: 100%;
  height: 8vh;
  top: 0;
  left: 0;
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
  transition: all 0.6s ease;

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
  height: 100%;
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
  position: fixed;
  padding: 0.6em 1em;
  width: 100%;
  height: 10vh;
  z-index: 100;
  background: white;
  justify-content: space-between;
  align-items: center;
  border-bottom: 2px solid $font-dark;

  a {
    font-weight: bold;
    color: $font-dark;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

@media screen and (min-width: 768px) {
  #nav {
    display: flex;

    img {
      height: 100%;
    }

    .links {
      display: flex;
      justify-content: space-around;
      width: 50%;

      a {
        display: block;
        font-size: 1.25rem;
        text-decoration: none;
      }
    }
  }

  .nav-mobile-container {
    display: none;
  }
}

@media screen and (min-width: 1024px) {
  #nav {
    height: 9vh;
    padding: 0.6em 1.5em 0.6em 1.5em;

    img {
      margin-left: 1em;
    }
    .links {
      width: 40%;
      a {
        font-size: 1.1rem;
      }
    }
  }
}
</style>
