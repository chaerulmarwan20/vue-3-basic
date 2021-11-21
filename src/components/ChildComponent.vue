<template>
  <div>{{ text }}</div>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      default: "Child Component",
    },
  },
};
</script>
