<template>
  <section class="container">
    <NuxtLink to="/results">Organism: results page</NuxtLink>
    <div>
      <p>Logo shall be Green</p>
      <app-logo-green />
      <hr />
      <p>Logo shall be Red</p>
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
