<template>
  <v-container>
    <AddTodo v-on:add-todo="addTodo" />
    <h1 style="color: #335eea">Todos</h1>
    <div v-bind:key="todo.id" v-for="todo in todos">
      <TodoItem v-bind:todo="todo" v-on:del-todo="deleteTodo" />
    </div>
  </v-container>
</template>

<script>
import TodoItem from "./TodoItem";
import AddTodo from "./AddTodo";
import axios from "axios";
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
      axios
        .delete(`https://jsonplaceholder.typicode.com/todos/${id}`)
        .then(
          (res) => ((this.todos = this.todos.filter((todo) => todo.id !== id)), res.Data)
        )
        .catch((err) => console.log(err));
    },
    addTodo(newTodo) {
      const { title, completed } = newTodo;
      axios
        .post("https://jsonplaceholder.typicode.com/todos", {
          title,
          completed,
        })
        .then((res) => (this.todos = [...this.todos, res.Data]))
        .catch((err) => console.log(err));
    },
    created() {
      axios
        .get("https://jsonplaceholder.typicode.com/todos?_limit=10")
        .then((res) => (this.todos = res.data))
        .catch((err) => console.log(err));
    },
  },
};
</script>

<style></style>
