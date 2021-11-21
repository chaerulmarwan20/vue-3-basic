<template>
  <child-component ref="childComponent" @child-click="onPress" />
  <button @click="clickMe">Button from Parent Component</button>
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  components: { ChildComponent },
  methods: {
    onPress(val) {
      console.log(val);
    },
    clickMe() {
      this.$refs.childComponent.onClick();
    },
  },
};
</script>
