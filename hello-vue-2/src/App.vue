<template>
  <div>Hello</div>
  <teleport to="#portal-root">
    <Portal />
  </teleport>
</template>

<script>
import Portal from './components/Portal.vue';

export default {
  name: 'App',
  data() {
    return {};
  },
  methods: {},
  components: { Portal },
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h4 {
  color: green;
}
</style>
