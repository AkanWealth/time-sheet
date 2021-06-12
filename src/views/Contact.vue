<template>
  <v-container fluid fill-height>
    <v-layout align-center justify-center>
      <v-flex xs12 sm8 md4 lg4>
        <v-card class="elevation-1 pa-3">
          <v-card-text>
            <div class="layout column align-center">
              <!-- <img
                  src="static/logo.png"
                  alt="Vue Material Admin"
                  width="180"
                  height="180"
                /> -->
              <h2 class="flex my-4" style="color: #ff6584">Contact</h2>
            </div>
            <v-form>
              <v-text-field v-model="fullName" label="Full Name" required></v-text-field>
              <v-text-field v-model="email" label="E-mail" required></v-text-field>
              <v-textarea v-model="message" label="Message" required></v-textarea>
            </v-form>
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn block color="primary">Submit</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: "contact",
  data() {
    return {
      fullName: "",
      email: "",
      message: "",
    };
  },
};
</script>

<style lang="scss" scoped></style>
