<template>
  <div>Component C</div>
  <ComponentE />
</template>

<script>
import ComponentE from './ComponentE.vue';

export default {
  name: 'ComponentC',
  components: { ComponentE },
};
</script>

<style scoped></style>
