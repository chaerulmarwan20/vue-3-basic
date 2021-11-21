<template>
  <div :class="status ? 'success' : 'danger'">Status</div>
  <button @click="status = !status">Change</button>
  <div :class="[boldClass, greenClass]">Hello World</div>
</template>

<script>
export default {
  data() {
    return {
      status: true,
      boldClass: "bold",
      greenClass: "success",
    };
  },
};
</script>

<style>
.success {
  color: green;
}
.danger {
  color: red;
}
.bold {
  font-weight: 700;
}
</style>
