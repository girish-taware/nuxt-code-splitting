<template>
  <section class="container">
    <NuxtLink to="/">Organism: home page</NuxtLink>
    <div>
      <p><strong>Logo shall be Red</strong></p>
      <app-logo-red />
      <hr />
      <p><strong>Logo shall be Green</strong></p>
      <app-logo-green />
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
  margin: 24px;
}

hr {
  margin: 15px;
}
</style>
