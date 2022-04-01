<template>
  <div class="giri-logo-red-container">
    <div class="giri-logo-red-title">
      <strong>AppLogoRed Molecule Component</strong>: RED text
    </div>
    <div class="giri-logo-red-text">This shall be red text</div>
    <div class="giri-logo-red-triangle">
      <div class="Triangle Triangle--two" />
      <div class="Triangle Triangle--one" />
      <div class="Triangle Triangle--three" />
      <div class="Triangle Triangle--four" />
    </div>
    <app-logo></app-logo>
    <Subtitle class="giri-pink-color" />
  </div>
</template>

<script>
import AppLogo from "~/components/AppLogo.vue";
import Subtitle from "~/components/Subtitle.vue";

export default {
  components: {
    AppLogo,
    Subtitle,
  },
};
</script>

<style>
app-logo {
  /* app-logo is component similar to components such as ecw-text, ecw-button */
  color: #803b44; /* no conflict warning because it's not used in AppLogoGreen Component */
  margin-right: 20px; /* no conflict warning same as above */
  margin-left: 21px;
  /* 
    margin-left generates conflict warning as below because it's used in AppLogoGreen Component

    console warning
    ./node_modules/extract-css-chunks-webpack-plugin/dist/loader.js
    ??ref--3-oneOf-1-0!./node_modules/css-loader/dist/cjs.js
    ??ref--3-oneOf-1-1!./node_modules/vue-loader/lib/loaders/stylePostLoader.js!./node_modules/postcss-loader/src
    ??ref--3-oneOf-1-2!./node_modules/vue-loader/lib
    ??vue-loader-options!./components/AppLogoRed.vue?vue&type=style&index=0&lang=css&

    From the above console warning, we can see that the conflict is in AppLogoRed.vue
  */
}

.giri-logo-red-container {
  color: rgb(252, 112, 94);
}

.giri-logo-red-title {
  color: red;
}

.giri-logo-red-text {
  color: red;
}

.giri-pink-color {
  color: pink;
}

.giri-logo-red-triangle {
  display: inline-block;
  animation: turn 2s linear forwards 1s;
  transform: rotateX(180deg);
  position: relative;
  overflow: hidden;
  height: 180px;
  width: 245px;
}

.giri-logo-red-triangle .Triangle {
  position: absolute;
  top: 0;
  left: 0;
  width: 0;
  height: 0;
}

.giri-logo-red-triangle .Triangle--one {
  border-left: 105px solid transparent;
  border-right: 105px solid transparent;
  border-bottom: 180px solid red;
}

.giri-logo-red-triangle .Triangle--two {
  top: 30px;
  left: 35px;
  animation: goright 0.5s linear forwards 3.5s;
  border-left: 87.5px solid transparent;
  border-right: 87.5px solid transparent;
  border-bottom: 150px solid #803b44;
}

.giri-logo-red-triangle .Triangle--three {
  top: 60px;
  left: 35px;
  animation: goright 0.5s linear forwards 3.5s;
  border-left: 70px solid transparent;
  border-right: 70px solid transparent;
  border-bottom: 120px solid #35495e;
}

.giri-logo-red-triangle .Triangle--four {
  top: 120px;
  left: 70px;
  animation: godown 0.5s linear forwards 3s;
  border-left: 35px solid transparent;
  border-right: 35px solid transparent;
  border-bottom: 60px solid #fff;
}

@keyframes turn {
  100% {
    transform: rotateX(0deg);
  }
}

@keyframes godown {
  100% {
    top: 180px;
  }
}

@keyframes goright {
  100% {
    left: 70px;
  }
}
</style>
