<template>
  <div id="app">
    <h1>{{name}}</h1>
    <button v-on:click="name= 'Batman'">Change name</button>
    <h1>{{count}}</h1>
    <button v-on:click="count +=1">increment</button>
    <!-- reset btn -->
    <button v-on:click="count = 0">reset</button>
    <button v-on:click="decrement(5)">decrement5</button>
<button v-on:click="decrement(1)">decrement1</button>

  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Vue.js",
      count: 0
    };
  },
  methods: {
    decrement(num) {
      this.count-=num;
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
