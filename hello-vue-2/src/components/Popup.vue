<template>
  <div>Popup Component</div>
  <input type="text" v-model="name" />
  <button @click="$emit('closePopup', name)">Close Popup</button>
</template>

<script>
export default {
  name: 'Popup',
  data() {
    return {
      name: '',
    };
  },
  emits: {
    closePopup: (name) => {
      if (!name) return false;
      else return true;
    },
  },
};
</script>

<style scoped></style>
