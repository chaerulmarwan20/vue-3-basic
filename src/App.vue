<template>
  <div class="container mt-4">
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">Simple Todo App</h5>
        <div class="row">
          <div class="col-10">
            <input
              type="text"
              v-model="todo"
              @keyup.enter="add"
              class="form-control"
            />
          </div>
          <div class="col-2">
            <button type="button" class="btn btn-success" @click="add">
              Add
            </button>
          </div>
        </div>
        <list :todos="todos" @deleteTodo="deleteTodo" @doneTodo="doneTodo" />
        <small>Total Todo : {{ totalTodo }}</small>
      </div>
    </div>
  </div>
</template>

<script>
import List from "./components/List.vue";

export default {
  components: {
    List,
  },
  data() {
    return {
      todo: "",
      todos: [],
    };
  },
  mounted() {
    const todosLocal = localStorage.getItem("todos");
    this.todos = todosLocal ? JSON.parse(todosLocal) : [];
  },
  computed: {
    totalTodo() {
      return this.todos.length;
    },
  },
  methods: {
    add() {
      this.todos.unshift({
        activity: this.todo,
        isDone: false,
      });
      this.todo = "";
      this.saveToLocalStorage();
    },
    deleteTodo(todoIdx) {
      this.todos = this.todos.filter((item, idx) => {
        if (idx !== todoIdx) return item;
      });
      this.saveToLocalStorage();
    },
    doneTodo(todoIdx) {
      this.todos = this.todos.filter((item, idx) => {
        if (idx === todoIdx) item.isDone = !item.isDone;
        return item;
      });
      this.saveToLocalStorage();
    },
    saveToLocalStorage() {
      localStorage.setItem("todos", JSON.stringify(this.todos));
    },
  },
};
</script>
