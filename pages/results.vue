<template>
  <section class="container">
    <div>
      <app-logo-red />
      <hr />
      <app-logo-green />
    </div>
  </section>
</template>

<script>
import AppLogoRed from "~/components/AppLogoRed.vue";
import AppLogoGreen from "~/components/AppLogoGreen.vue";

export default {
  components: {
    AppLogoRed,
    AppLogoGreen,
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
