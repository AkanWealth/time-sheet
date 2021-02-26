<template>
  <div class="todo-item" v-bind:class="{ 'is-complete': todo.completed }">
    <p>
      <v-checkbox v-on:change="markComplete"
    >{{ todo.title }}</v-checkbox>
<!--       <input type="checkbox" v-on:change="markComplete" />
      {{ todo.title }} -->
      <v-btn @click="$emit('del-todo', todo.id)" class="del" color="#ff0000" dark rounded
        >x</v-btn
      >
    </p>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed;
    },
  },
};
</script>

<style scoped>
.todo-item {
  background: #f4f4f4;
  padding: 10px;
  border-bottom: 1px #ccc dotted;
}
.is-complete {
  text-decoration: line-through;
}
.del {
  border: none;
  padding: 5px 9px;
  cursor: pointer;
  float: right;
}
</style>
