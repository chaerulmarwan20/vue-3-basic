<template>
  <div>Parent Component</div>
  <child-component text="Hello World" />
  <child-component :text="message" />
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  data() {
    return {
      message: "From Message",
    };
  },
  components: { ChildComponent },
};
</script>
