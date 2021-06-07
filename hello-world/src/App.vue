<template>
  <!-- Binding text -->
  <div>{{ greet }} {{ name }}</div>
  <div v-text="channel"></div>

  <!-- Binding html -->
  <div v-html="channel"></div>

  <!-- Binding attributes -->
  <h2 :id="headingId">Heading</h2>
  <button :disabled="isDisabled">Bind</button>

  <!-- Binding classes -->
  <div class="underline">Underlined text</div>
  <h2 class="underline" :class="status">Status</h2>
  <h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 :class="isSoldOut ? 'soldOut' : 'new'">Soldout? Movie</h2>
  <h2 :class="['new', 'promoted']">Newly promoted movie</h2>
  <h2 :class="[isPromoted && 'promoted', isSoldOut ? 'soldOut' : 'new']">
    Array conditional movie
  </h2>
  <h2
    :class="{
      promoted: isPromoted,
      new: !isSoldOut,
      soldOut: isSoldOut,
    }"
  ></h2>

  <!-- Binding styles -->
  <h2
    :style="{
      color: highlightColor,
      'font-size': headerSize + 'px',
      fontWeight: 'bold',
      padding: '20px',
    }"
  >
    Inline Style
  </h2>
  <h2 :style="headerStyleObject">Inline style with object</h2>
  <div :style="[baseStyleObject, successStyleObject]">
    Inline Styles - Array syntax
  </div>
  <div :style="[baseStyleObject, dangerStyleObject]">
    Inline Styles - Array syntax
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      greet: 'Hello',
      name: 'Rajat Verma',
      channel: '<b>Codevolution<b>',
      headingId: 'heading',
      isDisabled: true,
      status: 'danger',
      isPromoted: false,
      isSoldOut: true,
      highlightColor: 'orange',
      headerSize: '50',
      headerStyleObject: {
        color: 'orange',
        fontSize: '50px',
        padding: '20px',
      },
      baseStyleObject: {
        fontSize: '50px',
        padding: '10px',
      },
      successStyleObject: {
        color: 'green',
        backgroundColor: 'lightGreen',
        border: '1px solid green',
        padding: '20px',
      },
      dangerStyleObject: {
        color: 'darked',
        backgroundColor: 'red',
        border: '1px solid darked',
      },
    };
  },
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

.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: olivedrab;
}

.soldOut {
  color: red;
}
</style>
