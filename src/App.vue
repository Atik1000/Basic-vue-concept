<template>
  <div id="app">
    <h1>{{greet}}  {{ message }}</h1>

    <div v-text="channel"></div>
    <div v-text="message"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      greet: "Hello",
      message: "Welcome to Vue.js",
      channel: "Vue.js",
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
