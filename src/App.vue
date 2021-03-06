<template>
  <v-app>
    <v-app-bar app color="transparent" flat dark absolute>
      <div id="nav">
        <router-link
          id="title"
          to="/"
          style="color: #ff6584; margin-left: 3rem; font-size: 2.3rem"
          class="text-decoration-none"
          >Pace</router-link
        >
      </div>

      <v-spacer></v-spacer>
      <router-link to="/" class="text-decoration-none"> Home </router-link>
      <router-link to="/features" class="text-decoration-none">Features</router-link>
      <router-link to="/pricing" class="text-decoration-none">Pricing</router-link>
      <router-link to="/About" class="text-decoration-none">About</router-link>
      <router-link to="/contact" class="text-decoration-none">Contact</router-link>
      <v-spacer></v-spacer>
      <v-btn
        color="rgb(51,94,234)"
        to="/register"
        outlined
        plain
        class="text-decoration-none"
        x-large
      >
        <span class="mr-2">Get Started</span>
      </v-btn>
    </v-app-bar>

    <v-main class="container">
      <router-view />
    </v-main>
    <v-footer dark padless>
      <v-card class="flex" flat tile>
        <v-card-title class="primary">
          <strong class="subheading">Get connected with us on social networks!</strong>

          <v-spacer></v-spacer>

          <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
            <v-icon size="24px">
              {{ icon }}
            </v-icon>
          </v-btn>
        </v-card-title>

        <v-card-text class="py-2 white--text text-center">
          {{ new Date().getFullYear() }} — <strong>AkanWealth</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}
#title:hover {
  color: #335eea !important;
}
.text-decoration-none {
  font-size: x-large;
  margin-left: 2.5rem;
}
.text-decoration-none:hover {
  color: #ff6584;
}
</style>
