<template>
  <ul class="list-group w-50 m-auto mt-3">
    <li v-for="(todo, idx) in todos" :key="idx" class="list-group-item">
      <div class="d-flex justify-content-between align-items-center">
        <span v-if="todo.isDone" class="text-decoration-line-through">
          {{ todo.activity }}
        </span>
        <span v-else>{{ todo.activity }}</span>
        <div>
          <button type="button" @click="done(idx)" class="btn btn-info me-2">
            Done
          </button>
          <button type="button" @click="deleteTodo(idx)" class="btn btn-danger">
            X
          </button>
        </div>
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    todos: {
      type: Array,
      default: [],
    },
  },
  methods: {
    deleteTodo(idx) {
      this.$emit("deleteTodo", idx);
    },
    done(idx) {
      this.$emit("doneTodo", idx);
    },
  },
};
</script>
