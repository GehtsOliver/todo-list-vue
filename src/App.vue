<template>
  <v-app>
    <v-main>
      <v-container>
        <v-sheet class="mt-16 px-8 py-16" elevation="1" min-height="70vh" width="35vw">
          <Header @toggle-todo="toggleTodo" :text="addTodo ? 'Close' : 'Add Todo'" class="px-16" />
          <AddTodo v-if="addTodo" />
          <TodoList class="mt-16" :todos="todos" />
        </v-sheet>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Header from "./components/Header.vue";
import TodoList from "./components/TodoList.vue";
import AddTodo from "./components/AddTodo.vue";

export default {
  components: {
    Header,
    TodoList,
    AddTodo
  },
  data() {
    return {
      todos: [],
      addTodo: false
    }
  },
  methods: {
    toggleTodo() {
      console.log("toggle")
      this.addTodo = !this.addTodo;
    }
  }
  ,
  created() {
    this.todos = [
      {
        id: 1,
        text: "Wake up",
        time: "8am tomorrow",
        reminder: true
      },
      {
        id: 2,
        text: "Go to bed",
        time: "11pm tomorrow",
        reminder: false
      },
      {
        id: 3,
        text: "Clean flat",
        time: "3pm tomorrow",
        reminder: true
      },
    ]
  }

};
</script>
<style>
body {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
