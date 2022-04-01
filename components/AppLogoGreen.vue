<template>
  <div class="giri-logo-green-container">
    <div class="giri-logo-green-title">
      <strong>AppLogoGreen Molecule Component</strong>: Dark Green text
    </div>
    <div class="giri-logo-green-text">This shall be dark green text</div>
    <div class="giri-logo-green-triangle">
      <div class="Triangle Triangle--two" />
      <div class="Triangle Triangle--one" />
      <div class="Triangle Triangle--three" />
      <div class="Triangle Triangle--four" />
    </div>
    <app-logo></app-logo>
    <Subtitle />
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
  margin-left: 20px;
}

.giri-logo-green-container {
  color: lightgreen;
}

.giri-logo-green-title {
  color: darkgreen;
}

.giri-logo-green-text {
  color: darkgreen;
}

.giri-logo-green-triangle {
  display: inline-block;
  animation: turn 2s linear forwards 1s;
  transform: rotateX(180deg);
  position: relative;
  overflow: hidden;
  height: 180px;
  width: 245px;
}

.giri-logo-green-triangle .Triangle {
  position: absolute;
  top: 0;
  left: 0;
  width: 0;
  height: 0;
}

.giri-logo-green-triangle .Triangle--one {
  border-left: 105px solid transparent;
  border-right: 105px solid transparent;
  border-bottom: 180px solid #41b883;
}

.giri-logo-green-triangle .Triangle--two {
  top: 30px;
  left: 35px;
  animation: goright 0.5s linear forwards 3.5s;
  border-left: 87.5px solid transparent;
  border-right: 87.5px solid transparent;
  border-bottom: 150px solid #3b8070;
}

.giri-logo-green-triangle .Triangle--three {
  top: 60px;
  left: 35px;
  animation: goright 0.5s linear forwards 3.5s;
  border-left: 70px solid transparent;
  border-right: 70px solid transparent;
  border-bottom: 120px solid #35495e;
}

.giri-logo-green-triangle .Triangle--four {
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
