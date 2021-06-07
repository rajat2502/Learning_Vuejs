<template>
  Article Component
  <h2>{{ title }}</h2>
  <h2>Likes: {{ likes }}</h2>
  <h2>Published: {{ published ? 'YES' : 'NO' }}</h2>
</template>

<script>
export default {
  name: 'Article',
  props: {
    title: {
      type: String,
      required: true,
      default: 'Article Title',
    },
    likes: Number,
    published: Boolean,
  },
};
</script>

<style scoped></style>
