<template>
  <v-container fluid fill-height>
    <v-row class="text-center">
      <v-col cols="12">
        <div class="text-h4 font-weight-thin">Build in progress</div>
        <v-img
          :src="require('../assets/logo.png')"
          class="my-3"
          contain
          height="200"
        />
         <div class=" font-weight-thin">BENEDIKT WAGNER</div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "SplashScreen",

  data: () => ({}),
};
</script>
