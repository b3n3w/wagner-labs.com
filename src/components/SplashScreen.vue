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
        <div class="font-weight-thin">JUSTIN FABISCH</div>
      </v-col>
      <v-col>
        <v-btn icon href="https://www.linkedin.com/in/benedikt-wagner-808a101a9/" 
          ><v-icon left x-large>mdi-linkedin</v-icon></v-btn
        >
        <v-btn icon href="https://github.com/b3n3w" target="_blank">
          <v-icon right x-large>mdi-github</v-icon></v-btn
        >
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
