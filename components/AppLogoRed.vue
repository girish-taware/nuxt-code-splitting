<template>
  <div class="giri-logo-red-container">
    <div>*****START: AppLogoRed Component*****</div>
    <div class="giri-logo-red-title">
      <strong>Molecule Component</strong>: RED text
    </div>
    <div class="giri-logo-red-text">This shall be red text</div>
    <div class="giri-logo-red-triangle">
      <div class="Triangle Triangle--one" />
    </div>
    <app-info></app-info>
    <div>*****END: AppLogoRed Component*****</div>
  </div>
</template>

<script>
import AppInfo from "~/components/AppInfo.vue";

export default {
  components: {
    AppInfo,
  },
};
</script>

<style scoped>
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

.Triangle {
  position: absolute;
  top: 0;
  left: 0;
  width: 0;
  height: 0;
}

.Triangle--one {
  border-left: 105px solid transparent;
  border-right: 105px solid transparent;
  border-bottom: 180px solid red;
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
