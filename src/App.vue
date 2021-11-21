<template>
  <child-component>
    <!-- without destructuring object -->
    <template v-slot:default="props">
      <span>Judul : {{ props.data }}</span>
    </template>
    <template v-slot:slotContent="props">
      <span>Kontent : {{ props.data }}</span>
    </template>
    <!-- with destructuring object -->
    <template v-slot:slotFooter="{ data }">
      <span>Footer : {{ data }}</span>
    </template>
  </child-component>
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  components: { ChildComponent },
};
</script>
