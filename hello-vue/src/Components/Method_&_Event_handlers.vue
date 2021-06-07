<template>
  <!-- Methods -->
  <h2>Add method - {{ add(1, 2, 3) }}</h2>
  <h2>Multiply method - {{ multiply(baseValue) }}</h2>

  <!-- Event handling -->
  <h2>{{ name }}</h2>
  <div>
    <button @click="changeName($event), incrementCounter(1, $evenet)">
      Change Name
    </button>
  </div>

  <h2>Count: {{ count }}</h2>
  <div>
    <button @click="incrementCounter(2, $event)">Increment</button>
    <button @click="decrementCounter(4)">Decrement</button>
  </div>
</template>

<script>
export default {
  name: 'Method_Event_Handlers',
  data() {
    return {
      baseMultiplier: 5,
      baseValue: 4,
      name: 'Rajat',
      count: 0,
    };
  },
  methods: {
    // Don't use arrow functions for declaring the methods,
    //  Vue binds the data object to the methods
    add(a, b, c) {
      return a + b + c;
    },
    multiply(num) {
      return num * this.baseMultiplier;
    },
    changeName(e) {
      this.name = 'Batman';
      console.log(e);
    },
    incrementCounter(num, e) {
      this.count += num;
      console.log(e);
    },
    decrementCounter(num) {
      this.count -= num;
    },
  },
};
</script>

<style></style>
