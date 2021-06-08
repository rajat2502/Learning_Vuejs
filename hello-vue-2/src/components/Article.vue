<template>
  <div>
    Article Component
    <!-- to bind the non-prop attrs to element of your choice -->
    <h2 v-bind="$attrs">{{ title }}</h2>
    <h2>Likes: {{ likes }}</h2>
    <h2>Published: {{ published ? 'YES' : 'NO' }}</h2>
  </div>
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
  inheritAttrs: false,
};
</script>

<style scoped></style>
