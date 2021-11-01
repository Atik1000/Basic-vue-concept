<template>
  <div class="">
    <h2 v-if="num===0">The number is zero</h2>
    <h2 v-else-if="num===1">The number is one</h2>
    <h2 v-else>The number is not zero or one</h2>
<div v-if="display">
    <button @click="num=0">Zero</button>
    <button @click="num=1">One</button>
    <button @click="num=2">Two</button>
</div>
<h1 v-show="showElement
">Show V element</h1>
</div>
</template>

<script>
export default {
  data() {
    return {
     num: 10,
     display:false,
     showElement:true,
};
}
}
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
