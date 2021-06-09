<template>
  <h3 v-for="name in names" :key="name.firstName">
    <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
  </h3>
</template>

<script>
export default {
  name: 'NameList',
  data() {
    return {
      names: [
        { firstName: 'Rajat', lastName: 'Verma' },
        { firstName: 'Nihal', lastName: 'Pandey' },
        { firstName: 'Rohit', lastName: 'Agni' },
      ],
    };
  },
};
</script>

<style scoped></style>
