<template>
  <!-- <Greet name="Rajat" heroName="Batman" />
  <Greet name="Diana" heroName="Spiderman" />
  <Greet :name="name" :heroName="heroName" /> -->

  <!-- <Article id="my-article" title="Hello World" :likes="50" :published="true" /> -->

  <!-- <h2>App component {{ name }}</h2>
  <ComponentC /> -->

  <button @click="showPopup = true" :disabled="showPopup">Show Popup</button>
  <Popup v-if="showPopup" @closePopup="closePopup" />
</template>

<script>
// import Greet from './components/Greet.vue';
// import Article from './components/Article.vue';
// import ComponentC from './components/ComponentC.vue';
import Popup from './components/Popup.vue';

export default {
  name: 'App',
  data() {
    return {
      name: 'Keshav',
      heroName: 'Motu',
      showPopup: false,
    };
  },
  methods: {
    closePopup(name) {
      console.log(name);
      this.showPopup = false;
    },
  },
  provide() {
    return { username: this.name };
  },
  components: { Popup },
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
