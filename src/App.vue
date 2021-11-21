<template>
  <div>{{ total }}</div>
  <input type="text" v-model="num1" />
  <input type="text" v-model="num2" />
</template>

<script>
export default {
  data() {
    return {
      num1: 0,
      num2: 0,
    };
  },
  computed: {
    total() {
      return parseInt(this.num1) + parseInt(this.num2);
    },
  },
};
</script>
