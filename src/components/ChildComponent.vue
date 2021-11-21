<template>
  <div>
    <span>Child Component</span>
    <button @click="onPress">Click from Child</button>
  </div>
</template>

<script>
export default {
  emits: ["child-click"],
  methods: {
    onClick() {
      console.log("Click Me");
    },
    onPress() {
      this.$emit("child-click", "Value from Child");
    },
  },
};
</script>
