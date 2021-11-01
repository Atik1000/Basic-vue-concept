<template>
  <div id="app">
    <div v-for="name in names" :key="name">
      <h2 v-if="name ==='Bruce' ">
        <span>{{ name }}</span>
      </h2>

    </div>
  
    <button @click="shuffle">Shuffle</button>
  </div>
</template>

<script>
import _ from "lodash";
export default {
  name: "App",
  data() {
    return {
      names: ["Bruce", "Clark", "Diana", "Barry"],
    };
  },
  methods: {
    shuffle() {
      console.log(this.names);
      this.names = _.shuffle(this.names);
    },
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
