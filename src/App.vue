<template>
  <pre>{{ $data }}</pre>
  <button @click="onPress">Click Me</button>
</template>

<script>
import basicMixins from "./mixins/basic";
import merge from "./mixins/merge";

export default {
  mixins: [basicMixins, merge],
  data() {
    return {
      name: "Chaerul",
    };
  },
};
</script>
