<template>
  <div>Component F {{ username }}</div>
</template>

<script>
export default {
  name: 'ComponentF',
  inject: ['username'],
};
</script>

<style scoped></style>
