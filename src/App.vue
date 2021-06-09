<template>
  <v-app>
    <v-main>
      <splash-screen />
    </v-main>
  </v-app>
</template>

<script>
import SplashScreen from "./components/SplashScreen.vue";
export default {
  name: "App",

  components: {
    SplashScreen,
  },

  data: () => ({
    //
  }),
};
</script>
