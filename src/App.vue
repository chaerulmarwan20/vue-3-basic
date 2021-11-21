<template>
  <div>{{ message }}</div>
  <input type="text" v-model="message" />
</template>

<script>
export default {
  data() {
    return {
      message: "Hello World",
    };
  },
  watch: {
    message(value) {
      console.log("Perubahan di message " + value);
    },
  },
};
</script>
