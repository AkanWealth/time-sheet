<template>
  <v-app>
    <Layout />
    <router-view />
    <FooterBar />
  </v-app>
</template>

<script>
import Layout from "./components/Layout.vue";
import FooterBar from "./components/FooterBar.vue";
export default {
  name: "App",
  components: {
    Layout,
    FooterBar,
  },
  data: () => ({
    // navLinks: [
    //   {
    //     text: "Contact",
    //     path: "/contact",
    //     icon: "ion-ios-megaphone",
    //   },
    //   {
    //     text: "About",
    //     path: "/about",
    //     icon: "ion-ios-business",
    //   },
    //   {
    //     text: "Blog",
    //     path: "/blog",
    //     icon: "ion-ios-bonfire",
    //   },
    //   {
    //     text: "Portfolio",
    //     path: "/portfolio",
    //     icon: "ion-ios-briefcase",
    //   },
    // ],
  }),
  /* methods: {
    handleView() {
      this.mobileView = window.innerWidth <= 990;
      window.addEventListener("resize", this.handleView);
    },
  }, */
  /* created() {
    this.handleView();
  }, */
};
</script>
<style>
* {
  box-sizing: border-box;
}
body {
  font-family: Arial, Helvetica, sans-serif;
}
/* #icon {
  padding: 10px 10px 20px;
  margin: 1rem 2rem 3rem 2rem;
  width: 70px;
  height: 70px;
} */
/* .open {
  transform: translateY(300px);
} */
</style>
