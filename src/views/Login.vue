<template>
  <v-container>
    <h2 style="color: rgb(51, 94, 234)">Login</h2>
    <!-- another form -->
    <form style="width: 30rem">
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

      <v-btn class="mr-4" @click="submit" color="primary"> Login </v-btn>
      <v-btn to="/register" class="text-decoration-none" color="#ff6584" dark>
        SignUp
      </v-btn>
    </form>
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
<style scoped></style>
