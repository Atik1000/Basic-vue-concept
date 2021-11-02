<template>
  <div id="app">
    <h2>{{add(10,20,30,40)}}</h2>
    <h1>multiply {{multiply(baseValue)}}</h1>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      baseMultiplier: 5,
      baseValue: 10,
    };
  },
  methods: {
    add(a,b,c) {
      return a+=b+=c;
    },
    multiply(num){
      return num * this.baseMultiplier;
    }
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
