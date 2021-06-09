<template
  ><h3>PostList Component</h3>
  <button @click="getPosts">Load Post</button>

  <h3 v-if="errorMsg">{{ errorMsg }}</h3>
  <div v-for="post in posts" :key="post.id">
    <h3>{{ post.id }}. {{ post.title }}</h3>
    <p>{{ post.body }}</p>
    <hr />
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'PostList',
  data() {
    return {
      posts: [],
      errorMsg: '',
    };
  },
  methods: {
    getPosts() {
      axios
        .get('https://jsonplaceholder.typicode.com/posts')
        .then((res) => (this.posts = res.data))
        .catch((err) => (this.errorMsg = 'Error retriving data'));
    },
  },
};
</script>

<style scoped></style>
