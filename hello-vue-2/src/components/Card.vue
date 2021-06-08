<template>
  <div id="header"><slot name="header"></slot></div>
  <div id="content"><slot>Default content</slot></div>
  <div id="footer"><slot name="footer"></slot></div>
</template>

<script>
export default {
  name: 'Card',
  props: ['content'],
};
</script>

<style scoped></style>
