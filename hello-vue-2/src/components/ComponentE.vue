<template>
  <div>Component E</div>
  <ComponentF />
</template>

<script>
import ComponentF from './ComponentF.vue';

export default {
  name: 'ComponentE',
  components: { ComponentF },
};
</script>

<style scoped></style>
