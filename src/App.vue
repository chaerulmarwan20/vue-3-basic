<template>
  <child-component message="Hello World" :number="11" />
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  components: { ChildComponent },
};
</script>
