<template>
  <component-satu />
</template>

<script>
import ComponentSatu from "./components/ComponentSatu.vue";

export default {
  data() {
    return {
      author: "Chaerul",
    };
  },
  provide() {
    return {
      providedAuthor: this.author,
    };
  },
  components: { ComponentSatu },
};
</script>
