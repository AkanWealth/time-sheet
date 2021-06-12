<template>
  <v-app-bar color="transparent" app flat dense absolute height="55rem">
    <v-app-bar-nav-icon @click="$emit('open-drawer')" style="margin-top: 0.5rem" />

    <v-toolbar-title
      ><router-link to="/" class="toolbar-title">Pace</router-link></v-toolbar-title
    >
    <v-spacer></v-spacer>
    <v-toolbar-items class="shrink mt-1 hidden-sm-and-down">
      <router-link to="/" class="toolbar-item"> Home </router-link>
      <router-link to="/features" class="toolbar-item">Features</router-link>
      <router-link to="/pricing" class="toolbar-item">Pricing</router-link>
      <router-link to="/About" class="toolbar-item">About</router-link>
      <router-link to="/contact" class="toolbar-item">Contact</router-link>
    </v-toolbar-items>
    <v-spacer></v-spacer>
    <v-btn to="/register" outlined id="getStarted" class="shrink mt-1 hidden-sm-and-down"
      >GET STARTED</v-btn
    >
  </v-app-bar>
</template>
<script></script>
<style scoped>
.toolbar-title {
  color: #335eea;
  margin-top: 0.5rem;
  padding: 25px;
  font: bolder;
  font-size: 1.7rem;
  text-decoration: none;
}
.toolbar-item {
  padding: 20px;
  text-decoration: none;
  color: #ff6584;
  font: bold;
  font-size: 1.3rem;
}
a.router-link-exact-active {
  color: #335eea;
}
#getStarted {
  background: transparent;
  text-decoration: none;
}
</style>
