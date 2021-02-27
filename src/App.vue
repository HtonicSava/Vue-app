<template>
  <div id="app">
    <div class="content">
      <DesireCard />
      <AuthorizationCard />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "./components/HelloWorld.vue";
import AuthorizationCard from "./components/AuthorizationCard.vue";
import DesireCard from "./components/DesireCard.vue";

@Component({
  components: {
    AuthorizationCard,
    DesireCard
  }
})
export default class App extends Vue {}
</script>

<style lang="scss">
@font-face {
  font-family: "inter";
  src: url("~@/assets/fonts/Inter-VariableFont_slnt,wght.ttf") format("woff");
  // font-weight: 500;
  font-style: normal;
}

#app {
  font-family: Inter, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-image: url("./assets/background.png");
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  width: 1920px;
  height: 1083px;
  left: 0px;
  top: -3px;
}

.content {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-left: 36px;
  filter: drop-shadow(0px 9px 28px rgba(0, 0, 0, 0.1));
}

.AuthorizationCard {
  position: relative;
  left: -56px;
}

* {
  padding: 0;
  margin: 0;
  border: 0;
}
*,
*:before,
*:after {
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
}
:focus,
:active {
  outline: none;
}
a:focus,
a:active {
  outline: none;
}
nav,
footer,
header,
aside {
  display: block;
}
html,
body {
  height: 100%;
  width: 100%;
  font-size: 100%;
  line-height: 1;
  // font-size: 14px;
  -ms-text-size-adjust: 100%;
  -moz-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
input,
button,
textarea {
  font-family: inherit;
}
input::-ms-clear {
  display: none;
}
button {
  cursor: pointer;
}
button::-moz-focus-inner {
  padding: 0;
  border: 0;
}
a,
a:visited {
  text-decoration: none;
}
a:hover {
  text-decoration: none;
}
ul li {
  list-style: none;
}
img {
  vertical-align: top;
}
a {
  color: inherit;
}
h1,
h2,
h3,
h4,
h5,
h6 {
  font-size: inherit;
  font-weight: inherit;
}
</style>
