<template>
  <button @click="activeTab = 'TabA'">Tab A</button>
  <button @click="activeTab = 'TabB'">Tab B</button>
  <button @click="activeTab = 'TabC'">Tab C</button>

  <!-- <TabA v-if="activeTab === 'TabA'" />
  <TabB v-else-if="activeTab === 'TabB'" />
  <TabC v-else /> -->

  <keep-alive>
    <component :is="activeTab" />
  </keep-alive>
</template>

<script>
import TabA from './components/TabA.vue';
import TabB from './components/TabB.vue';
import TabC from './components/TabC.vue';

export default {
  name: 'App',
  data() {
    return {
      activeTab: 'TabA',
    };
  },
  methods: {},
  components: { TabA, TabB, TabC },
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
