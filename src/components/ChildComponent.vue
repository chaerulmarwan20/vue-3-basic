<template>
  <div>Title</div>
  <slot :data="title" />
  <div>Content</div>
  <slot name="slotContent" :data="content" />
  <div>Footer</div>
  <slot name="slotFooter" :data="footer" />
</template>

<script>
export default {
  data() {
    return {
      title: "Hello World",
      content: "I'm Content",
      footer: "Footer Here",
    };
  },
};
</script>
