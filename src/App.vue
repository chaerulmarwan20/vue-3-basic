<template>
  <div>{{ message }}</div>
  <!-- <child-component
    :model-value="message"
    @update:model-value="message = $event"
  /> -->
  <!-- sama dengan -->
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
