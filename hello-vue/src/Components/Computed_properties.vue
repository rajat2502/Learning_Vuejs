<template>
  <h2>{{ firstName }} {{ lastName }}</h2>
  <h2>{{ fullName }}</h2>

  <!-- Computed Setter -->
  <button @click="changeFullName">Change Full Name</button>

  <!-- v-for and computed properties -->
  <template v-for="item in items" :key="item.name">
    <h2 v-if="item.price > 100">{{ item.title }}: {{ item.price }}</h2>
  </template>

  <!-- recommended approach -->
  <h2 v-for="item in expensiveItems" :key="item.name">
    {{ item.title }}: {{ item.price }}
  </h2>
</template>

<script>
export default {
  name: 'Computed_Properties',
  data() {
    return {
      firstName: 'Rajat',
      lastName: 'Verma',
      items: [
        { id: 1, title: 'TV', price: 100 },
        { id: 2, title: 'Phone', price: 200 },
        { id: 3, title: 'Laptop', price: 300 },
      ],
    };
  },
  methods: {
    changeFullName() {
      this.fullName = 'Clark kent';
    },
  },
  computed: {
    fullName: {
      get() {
        return `${this.firstName} ${this.lastName}`;
      },
      set(value) {
        const names = value.split(' ');
        this.firstName = names[0];
        this.lastName = names[1];
      },
    },
    expensiveItems() {
      return this.items.filter((i) => i.price > 100);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
