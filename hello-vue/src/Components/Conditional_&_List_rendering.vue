<template>
  <!-- v-if, v-else, v-else-if -->
  <h2 v-if="num === 0">The number is zero</h2>
  <h2 v-else-if="num > 0">The number is positive</h2>
  <h2 v-else-if="num < 0">The number is negative</h2>
  <h2 v-else>Not a Number</h2>

  <template v-if="display">
    <h2>Vishwas</h2>
    <h2>Codevolution</h2>
    <h2>Vue</h2>
  </template>

  <!-- v-show => it is always present in the dom even if the condition is false -->
  <!-- If you have an element that needs to be hide and show again and again then go for v-show as it just sets the display property while v-if mounts the element -->
  <h2 v-show="showElement">v-show</h2>
  <h2 v-if="showElement">v-if</h2>

  <!-- List rendering -->
  <h2 v-for="(name, index) in names" :key="index">{{ index }}. {{ name }}</h2>
  <h2 v-for="name in fullNames" :key="name.first">
    {{ name.first }} {{ name.last }}
  </h2>
  <div v-for="actor in actors" :key="actor.name">
    <h2>{{ actor.name }}</h2>
    <h3 v-for="movie in actor.movies" :key="movie">{{ movie }}</h3>
  </div>
  <h2 v-for="(value, key, index) in myInfo" :key="value">
    {{ index }}. {{ key }}: {{ value }}
  </h2>

  <template v-for="name in names" :key="name">
    <h2>{{ name }}</h2>
    <hr />
  </template>

  <!-- Condtional list rendering -->
  <template v-for="name in names" :key="name">
    <h2 v-if="name === 'Bruce'">{{ name }}</h2>
  </template>
</template>

<script>
export default {
  name: 'Conditional_List_rendering',
  data() {
    return {
      num: 1,
      display: true,
      showElement: true,
      names: ['Bruce', 'Clark', 'Diana'],
      fullNames: [
        { first: 'Rajat', last: 'Verma' },
        { first: 'Annu', last: 'Verma' },
        { first: 'Nihal', last: 'Pandey' },
      ],
      actors: [
        { name: 'Christian Bale', movies: ['Batman', 'Clark', 'Diana'] },
        { name: 'Di Caprio', movies: ['Titanic', 'Inception'] },
      ],
      myInfo: {
        name: 'Vishwas',
        channel: 'Codevolution',
        course: 'Vue tutorial',
      },
    };
  },
};
</script>

<style></style>
