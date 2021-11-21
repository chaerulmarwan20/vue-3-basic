<template>
  <div id="lifecycle">{{ message }}</div>
  <button @click="message = 'Halo Dunia'">Update</button>
</template>

<script>
export default {
  data() {
    return {
      message: "Hello World",
    };
  },
  beforeCreate() {
    console.log("Before Create");
  },
  created() {
    console.log("Created");
    console.log(this.message);
    console.log(document.getElementById("lifecycle"));
  },
  beforeMount() {
    console.log("Before Mount");
  },
  mounted() {
    console.log("Mounted");
    console.log(this.message);
    console.log(document.getElementById("lifecycle"));
  },
  beforeUpdate() {
    console.log("Before Update");
    console.log(document.getElementById("lifecycle").textContent);
  },
  updated() {
    console.log("Updated");
    console.log(document.getElementById("lifecycle").textContent);
  },
  beforeUnmount() {
    console.log("Before Unmount");
  },
  unmounted() {
    console.log("Unmounted");
  },
};
</script>
