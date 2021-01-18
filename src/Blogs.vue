<template>
  <div id="blogs">
    <h2>Posts</h2>
    <div v-for="post in posts" :key="post.id">
      <h3>{{ post.title }}</h3>
      <p>{{ post.body | snippet }}</p>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Blogs",
  data() {
    return {
      posts: [],
    };
  },
  methods: {},

  created() {
    axios.get("https://jsonplaceholder.typicode.com/posts").then((response) => {
      console.log(response);
      this.posts = response.data;
    });
  },
};
</script>

<style>
</style>