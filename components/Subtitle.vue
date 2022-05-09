<template>
  <div class="giri-subtitle-container giri-subtitle-container-adaptable">
    <div>-----START: Subtitle Component-----</div>
    <div>div with no Subtitle Component css</div>
    <div class="css-conflict-study">div with Subtitle Component css</div>
    <div>-----END: Subtitle Component-----</div>
  </div>
</template>

<style scoped>
.giri-subtitle-container {
  color: dodgerblue;
}

/* will override the color of .giri-subtitle-container regardless of the placement of classname in div */
.giri-subtitle-container-adaptable {
  color: blue;
}

.css-conflict-study {
  color: dodgerblue;
}
</style>
