<template>
  <!-- <Greet name="Rajat" heroName="Batman" />
  <Greet name="Diana" heroName="Spiderman" />
  <Greet :name="name" :heroName="heroName" /> -->

  <Article title="Hello World" :likes="50" :published="true" />
</template>

<script>
// import Greet from './components/Greet.vue';
import Article from './components/Article.vue';

export default {
  name: 'App',
  data() {
    return {
      name: 'Keshav',
      heroName: 'Motu',
    };
  },
  components: { Article },
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
