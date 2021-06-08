<template>
  <Card></Card>
  <Card><h2>Card Content</h2></Card>
  <Card>Card Content</Card>
  <Card>
    <template v-slot:header>
      <h3>Header</h3>
    </template>

    <template v-slot:default>
      <h3>Card content</h3>
    </template>

    <template v-slot:footer>
      <h3>Footer</h3>
    </template>
  </Card>
</template>

<script>
import Card from './components/Card.vue';

export default {
  name: 'App',
  data() {
    return {};
  },
  methods: {},
  components: { Card },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
