<template>
  <div>Component Tiga</div>
  <div>{{ providedAuthor }}</div>
</template>

<script>
export default {
  inject: ["providedAuthor"],
};
</script>
