<template>
  <div>Title</div>
  <slot />
  <div>Content</div>
  <slot name="slotContent" />
  <div>Footer</div>
  <slot name="slotFooter" />
</template>

<script>
export default {};
</script>
