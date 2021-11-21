<template>
  <div class="demo-tab">
    <div v-for="(post, idx) in posts" :key="idx">
      <span>{{ post.name }}</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [],
    };
  },
  async created() {
    const res = await fetch("https://swapi.dev/api/planets");
    const { results } = await res.json();
    this.posts = results;
  },
};
</script>
