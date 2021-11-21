<template>
  <ol>
    <li v-for="(todo, idx) in todos" :key="todo.id">
      {{ idx }} - {{ todo.activity }}
    </li>
  </ol>
</template>

<script>
export default {
  data() {
    return {
      todos: [
        { id: 1, activity: "Futsal" },
        { id: 2, activity: "Badminton" },
        { id: 3, activity: "Basket" },
      ],
    };
  },
};
</script>
