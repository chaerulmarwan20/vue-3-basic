<template>
  <div>{{ message }}</div>
  <input type="text" v-model="message" />
  <!-- sama dengan -->
  <input type="text" :value="message" @input="message = $event.target.value" />
</template>

<script>
export default {
  data() {
    return {
      message: "Hi",
    };
  },
};
</script>
