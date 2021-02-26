<template>
  <v-container>
    <AddTodo v-on:add-todo="addTodo" />
    <h1>Todos</h1>
    <div v-bind:key="todo.id" v-for="todo in todos">
      <TodoItem v-bind:todo="todo" v-on:del-todo="deleteTodo" />
    </div>
  </v-container>
</template>

<script>
import TodoItem from "./TodoItem";
import AddTodo from "./AddTodo";
export default {
  name: "Todos",
  components: {
    TodoItem,
    AddTodo,
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Todo one",
          completed: false,
        },
        {
          id: 2,
          title: "Todo two",
          completed: true,
        },
        {
          id: 3,
          title: "Todo three",
          completed: false,
        },
      ],
    };
  },
  methods: {
    deleteTodo(id) {
      this.todos = this.todos.filter((todo) => todo.id !== id);
    },
    addTodo(newTodo) {
      this.todos = [...this.todos, newTodo];
    },
  },
};
</script>

<style></style>
