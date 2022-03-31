<template>
  <section class="container">
    <div>
      <app-logo-green />
      <hr />
      <app-logo-red />
    </div>
  </section>
</template>

<script>
import AppLogoGreen from "~/components/AppLogoGreen.vue";
import AppLogoRed from "~/components/AppLogoRed.vue";

export default {
  components: {
    AppLogoGreen,
    AppLogoRed,
  },
};
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

hr {
  margin: 15px;
}
</style>
