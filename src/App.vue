<template>
  <div id="app">
    <!-- mastached -->
    <h1>{{ greet }} {{ message }}</h1>
    <!-- v-text -->
    <div v-text="channel"></div>
    <div v-html="message"></div>
    <!-- binding attribute -->
    <h2 v-bind:id="headingId">Heading</h2>
    <button v-bind:disabled="isDisabled">Submit</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      greet: "Hello",
      message: "<b>Welcome to Vue.js</b>",
      channel: "Vue.js",
      headingId:'heading',
      isDisabled:true
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
</style>
