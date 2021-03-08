<template>
  <div id="app">
    <the-header></the-header>
    <about></about>
    <projects></projects>
    <skills></skills>
    <work></work>
    <education></education>
    <the-footer></the-footer>
  </div>
</template>

<script>
import About from "./components/About.vue";
import Education from "./components/Education.vue";
import Skills from "./components/Skills.vue";
import Projects from "./components/Projects.vue";
import TheHeader from "./components/TheHeader.vue";
import Work from "./components/Work.vue";
import TheFooter from "./components/TheFooter.vue";
export default {
  components: {
    TheHeader,
    About,
    Education,
    Skills,
    Projects,
    Work,
    TheFooter,
  },
};
</script>

<style lang="scss">
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  width: 100%;
  height: 100vh;
  display: grid;
  grid-template-columns: 100%;
  grid-template-rows: 100% auto auto auto auto auto auto;
  overflow-x: hidden;
}
$darkPrimaryColor: #313131;
$darkSecondaryColor: #2c2c2c;
$terracotta: #e5765d;
$fontColor: #e5e5e5;
$yellow: #ffb633;
* {
  box-sizing: border-box;
}
body {
  //font-size: calc(16px + (26 - 16) * ((100vw - 300px) / (1600 - 300)));
  // line-height: 1.5;
  background: $darkSecondaryColor;
  padding: 0;
  margin: 0;
  ::-webkit-scrollbar {
    width: 5px;
  }

  ::-webkit-scrollbar-track {
    box-shadow: inset 0 0 6px $darkSecondaryColor;
  }

  ::-webkit-scrollbar-thumb {
    background-color: $terracotta;
    outline: 1px solid $terracotta;
  }
}

html,
body {
  height: 100%;
  overflow-x: hidden;
}
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Montserrat", sans-serif;
  color: $fontColor;
  letter-spacing: -0.08px;
  padding: 0;
  margin: 0;
}
h1 {
  font-size: 8rem;
  @media screen and (max-width: 375px) {
    font-size: 5rem;
  }
  @media screen and (max-width: 320px) {
    font-size: 5rem;
  }
}
h2 {
  font-size: 4rem;
  @media screen and (max-width: 320px) {
    font-size: 3rem;
  }
}
h3 {
  font-size: 2.5rem;
  @media screen and (max-width: 320px) {
    font-size: 2rem;
  }
}
h4 {
  font-size: 2rem;
  @media screen and (max-width: 320px) {
    font-size: 1.5rem;
  }
}
h5 {
  font-size: 1.5rem;
  font-weight: bold;
  @media screen and (max-width: 320px) {
    font-size: 1.2rem;
  }
}
h6 {
  font-size: 1rem;
  font-weight: bold;
}
img {
  max-width: 100%;
  width: 100%;
  height: auto;
}
p,
i,
span,
strong,
input,
button,
a,
li {
  font-family: "Montserrat", sans-serif;
  font-weight: 400;
  color: $fontColor;
  font-size: 16px;
}
a {
  text-decoration: none;
}
button {
  text-transform: uppercase;
  font-weight: 600;
}
</style>


