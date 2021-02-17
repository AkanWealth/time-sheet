<template>
  <v-app>
    <v-app-bar app color="transparent" flat dark>
      <v-app-bar-title class="title">Pace </v-app-bar-title>

      <v-spacer></v-spacer>
      <v-btn
        class="ma-2"
        color="indigo"
        target="_blank"
        plain
        to="/src/components/HelloWorld.vue"
        >Home
      </v-btn>
      <v-btn
        class="ma-2"
        color="indigo"
        target="_blank"
        plain
        to="/src/components/About.vue"
        >Features
      </v-btn>
      <v-btn class="ma-2" color="indigo" target="_blank" plain>Pricing </v-btn>
      <v-btn class="ma-2" color="indigo" target="_blank" plain>About </v-btn>
      <v-btn class="ma-2" color="indigo" target="_blank" plain>contact </v-btn>
      <v-spacer></v-spacer>

      <v-btn class="ma-2" color="indigo" target="_blank" outlined plain>
        <span class="mr-2">Get Started</span>
      </v-btn>
    </v-app-bar>

    <v-main>
      <HelloWorld />
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>
<style scoped>
.title {
  margin-left: 6rem;
  color: rgb(13, 13, 255);
  font-size: 20%;
}
.item {
  color: red;
}
</style>
