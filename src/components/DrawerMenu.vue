<template>
  <v-navigation-drawer :value="value" app @input="$emit('input', $event)">
    <v-list dense>
      <v-list-item
        class="btn"
        v-for="(item, index) in menu"
        :key="index"
        :to="item.link"
        link
      >
        <v-list-item-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>{{ item.name }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
      <v-list-item v-if="user">
        <v-btn
          href="javascript:void(0)"
          class="toolbar-item"
          outlined
          rounded
          @click="logout"
          >Logout</v-btn
        >
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
// import { mapGetters } from "vuex";
export default {
  name: "DrawerMenu",
  props: {
    value: {
      type: Boolean,
      required: true,
      default: false,
    },
  },
  data: () => ({
    menu: [
      {
        name: "Home",
        link: "/",
        icon: "mdi-home",
      },
      {
        name: "About",
        link: "/about",
        icon: "mdi-book",
      },
      {
        name: "Login",
        link: "/login",
        icon: "mdi-account-circle",
      },
      {
        name: "Sign Up",
        link: "/signup",
        icon: "mdi-account-plus",
      },
      {
        name: "Contact",
        link: "/contact",
        icon: "mdi-email",
      },
    ],
  }),

  // methods: {
  //   logout() {
  //     localStorage.removeItem("token");
  //     this.$store.dispatch("user", null);
  //     this.$router.push("/");
  //   },
  // },

  // computed: {
  //   ...mapGetters(["user"]),
  // },
};
</script>

<style scoped>
.toolbar-item {
  padding: 20px;
  text-decoration: none;
  color: #fff;
  background-color: teal;
  font: bold;
  font-size: 1.2rem;
  margin: 3rem;
}
</style>
