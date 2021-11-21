<template>
  <div>Parent Component</div>
  <child-component v-for="(todo, idx) in todos" :key="idx" :text="todo" />
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  data() {
    return {
      todos: ["Pertama", "Kedua", "Ketiga"],
    };
  },
  components: { ChildComponent },
};
</script>
