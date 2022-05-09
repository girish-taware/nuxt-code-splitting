<template>
  <div class="giri-logo-green-container">
    <div>*****START: AppLogoGreen Component*****</div>
    <div class="giri-logo-green-title">
      <strong>Molecule Component</strong>: Dark Green text
    </div>
    <div class="giri-logo-green-text">This shall be dark green text</div>
    <div class="giri-logo-green-triangle">
      <div class="Triangle Triangle--one" />
    </div>
    <app-info></app-info>
    <div>+++++START: SLOT+++++</div>
    <slot name="giri-content-for-subtitle"></slot>
    <div>+++++END: SLOT+++++</div>
    <div>*****END: AppLogoGreen Component*****</div>
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
  border-bottom: 180px solid #41b883;
}

.giri-subtitle-container {
   /* will be added to the subtitle because border is not scoped in subtitle component */
  border: 2px solid pink;
   /* will not change the scoped color of subtitle */
  color: pink;
}

.giri-subtitle-container-adaptable {
    /* will not change the scoped color of subtitle */
  color: red;
}

.css-conflict-study  {
  /* will be added to the subtitle because border is not scoped in subtitle component */
  border: 2px solid yellow;
  /* will not change the scoped color of subtitle */
  color: red;
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
