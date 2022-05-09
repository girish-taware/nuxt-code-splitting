<template>
  <section class="container">
    <NuxtLink to="/results">Organism: results page</NuxtLink>
    <div>
      <p><strong>Logo shall be Green</strong></p>
      <app-logo-green>
         <template #giri-content-for-subtitle>
           <Subtitle />
         </template>
      </app-logo-green>
      <hr />
      <p><strong>Logo shall be Red</strong></p>
      <app-logo-red />
    </div>
  </section>
</template>

<script>
import AppLogoGreen from "~/components/AppLogoGreen.vue";
import AppLogoRed from "~/components/AppLogoRed.vue";
import Subtitle from "~/components/Subtitle.vue";

export default {
  components: {
    AppLogoGreen,
    AppLogoRed,
    Subtitle
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

.giri-subtitle-container {
   /* will be overridden by style in AppLogoGreen which uses subtitle component */
  border: 2px solid black;
   /* will not change the scoped color of subtitle */
  color: black;
}

</style>
