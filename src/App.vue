<template>
  <div v-once>{{ message }}</div>
  <button @click="message = 'Halo Dunia'">Update</button>
</template>

<script>
export default {
  data() {
    return {
      message: "Hello World",
    };
  },
};
</script>
