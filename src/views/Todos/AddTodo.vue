<template>
  <v-container>
    <v-form @submit="addTodo">
      <input type="text" v-model="title" name="title" placeholder="Add Todo..." />
      <input type="submit" value="Submit" class="btn" />
      <!-- <v-btn @click="submit">Submit</v-btn> -->
    </v-form>
  </v-container>
</template>

<script>
export default {
  name: "AddTodo",
  data() {
    return {
      title: "",
    };
  },
  methods: {
    addTodo(e) {
      e.preventDefault();
      const newTodo = {
        title: this.title,
        completed: false,
      };
      // Send up to parent
      this.$emit("add-todo", newTodo);
      this.title = "";
    },
    /* submit() {
      this.formHasErrors = false;
      Object.keys(this.form).forEach((f) => {
        if (!this.form[f]) this.formHasErrors = true;
        this.$refs[f].validate(true);
      });
    }, */
  },
};
</script>

<style scoped>
v-form {
  display: flex;
}
input[type="text"] {
  flex: 10;
  padding: 8px;
}
input[type="submit"] {
  flex: 2;
  margin-left: 2rem;
}
.btn {
  display: inline-block;
  border: none;
  background: #ff6584;
  color: #fff;
  padding: 7px 20px;
  cursor: pointer;
}
btn:hover {
  background: #666;
}
</style>
