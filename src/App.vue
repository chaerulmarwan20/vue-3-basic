<template>
  <child-component>
    <template v-slot:default>
      <span>Slot Title</span>
    </template>
    <template v-slot:slotContent>
      <span>Slot Content</span>
    </template>
    <template v-slot:slotFooter>
      <span>Slot Footer</span>
    </template>
  </child-component>
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  components: { ChildComponent },
};
</script>
