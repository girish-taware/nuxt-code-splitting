<template>
  <section class="container">
    <NuxtLink to="/">Organism: home page</NuxtLink>
    <div>
      <p>Logo shall be Red</p>
      <app-logo-red />
      <hr />
      <p>Logo shall be Green</p>
      <app-logo-green />
    </div>
  </section>
</template>

<script>
export default {
  components: {
    AppLogoGreen: () => import("~/components/AppLogoGreen.vue"),
    AppLogoRed: () => import("~/components/AppLogoRed.vue"),
  },
};
</script>

<style scoped>
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
