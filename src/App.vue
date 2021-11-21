<template>
  <button @click="setStatus">Toggle</button>
  <div v-if="status">true</div>
  <div v-else>false</div>
</template>

<script>
export default {
  data() {
    return {
      status: true,
    };
  },
  methods: {
    setStatus() {
      this.status = !this.status;
    },
  },
};
</script>
