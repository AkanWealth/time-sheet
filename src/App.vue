<template>
  <v-app>
    <v-app-bar app color="transparent" flat dark fixed>
      <div class="d-flex align-center">
        <div id="title">
          <v-toolbar-title>
            <b class="myTitle">Pace</b>
          </v-toolbar-title>
        </div>
      </div>

      <v-spacer></v-spacer>
      <v-btn color="rgb(51,94,234)" to="/" plain class="text-decoration-none" x-large>
        Home
      </v-btn>
      <v-btn
        color="rgb(51,94,234)"
        to="/features"
        plain
        class="text-decoration-none"
        x-large
      >
        Features
      </v-btn>

      <v-btn
        color="rgb(51,94,234)"
        to="/pricing"
        plain
        class="text-decoration-none"
        x-large
      >
        Pricing
      </v-btn>
      <v-btn
        color="rgb(51,94,234)"
        to="/about"
        plain
        class="text-decoration-none"
        x-large
      >
        About
      </v-btn>
      <v-btn
        color="rgb(51,94,234)"
        to="/contact"
        plain
        class="text-decoration-none"
        x-large
      >
        Contact
      </v-btn>
      <v-spacer></v-spacer>

      <v-btn
        color="rgb(51,94,234)"
        to="/login"
        target="_blank"
        outlined
        plain
        class="text-decoration-none"
        x-large
      >
        <span class="mr-2">Get Started</span>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
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
.myTitle {
  color: rgb(51, 94, 234);
  margin-left: 3rem;
  font-size: 2.3rem;
}
</style>
