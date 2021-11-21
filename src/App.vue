<template>
  <div>{{ message }}</div>
  <hr />
  <child-component v-model="message" />
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  data() {
    return {
      message: "",
    };
  },
  components: { ChildComponent },
};
</script>
