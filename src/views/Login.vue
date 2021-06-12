<template>
  <v-container fluid fill-height>
    <v-row>
      <v-col cols="12" xs6 sm8 md4 lg4>
        <v-layout>
          <v-flex>
            <form>
              <v-text-field
                v-model="email"
                :error-messages="emailErrors"
                label="E-mail"
                required
                @input="$v.email.$touch()"
                @blur="$v.email.$touch()"
              ></v-text-field>
              <v-text-field
                v-model="password"
                :error-messages="passwordErrors"
                label="Password"
                required
                @input="$v.password.$touch()"
                @blur="$v.password.$touch()"
              ></v-text-field>
              <v-checkbox
                v-model="checkbox"
                :error-messages="checkboxErrors"
                label="Do you agree?"
                required
                @change="$v.checkbox.$touch()"
                @blur="$v.checkbox.$touch()"
              ></v-checkbox>

              <v-btn class="mr-4" @click="submit" color="primary" x-large dark>
                Login
              </v-btn>
              <v-btn
                to="/register"
                class="text-decoration-none"
                color="#ff6584"
                x-large
                dark
              >
                SignUp
              </v-btn>
            </form>
          </v-flex>
          <v-flex>
            <v-img alt="loginImg" class="loginPic" src="../assets/login-img.png" />
          </v-flex>
        </v-layout>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { validationMixin } from "vuelidate";
import { required, minLength, maxLength, email } from "vuelidate/lib/validators";

export default {
  mixins: [validationMixin],

  validations: {
    email: { required, email },
    password: { required, minLength: minLength(8), maxLength: maxLength(15) },
    checkbox: {
      checked(val) {
        return val;
      },
    },
  },

  data: () => ({
    email: "",
    password: "",
    checkbox: false,
  }),

  computed: {
    checkboxErrors() {
      const errors = [];
      if (!this.$v.checkbox.$dirty) return errors;
      !this.$v.checkbox.checked && errors.push("You must agree to continue!");
      return errors;
    },
    emailErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      !this.$v.email.email && errors.push("Must be valid e-mail");
      !this.$v.email.required && errors.push("E-mail is required");
      return errors;
    },
    passwordErrors() {
      const errors = [];
      if (!this.$v.password.$dirty) return errors;
      !this.$v.password.password && errors.push("Must be at least 8 character long");
      !this.$v.password.required && errors.push("Password is required");
      return errors;
    },
  },

  methods: {
    submit() {
      this.$v.$touch();
    },
  },
};
</script>
<style scoped>
.loginPic {
  width: 350px;
  margin-left: 5rem;
}
@media (max-width: 765px) {
  .loginPic {
    display: none;
  }
}
</style>
