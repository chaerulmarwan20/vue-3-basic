<template>
  <div v-html="message" />
</template>

<script>
export default {
  data() {
    return {
      message: "<span style='color: blue'>Biru</span>",
    };
  },
};
</script>
