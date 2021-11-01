<template>
  <div id="app">
    <!-- mastached -->
    <h1>{{ greet }} {{ message }}</h1>
    <!-- v-text -->
    <div v-text="channel"></div>
    <div v-html="message"></div>
    <!-- binding attribute -->
    <h2 v-bind:id="headingId">Heading</h2>
    <button v-bind:disabled="isDisabled" v-bind:class="status">Submit</button>
    <h2 class="uderline">Underline text</h2>
    <h2 v-bind:class="isPromoted && 'promoted'">Promoted</h2>
    <h1 v-bind:class="isSoldOut ? 'sold-out' : 'new'">Movie</h1>
    <h1
      v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'sold-out' : 'new']"
    >
      Array condition checker
    </h1>
    <!-- object condition movie -->
    <h1 v-bind:class="{ promoted: isPromoted, 'sold-out': isSoldOut,new:!soldOut }">Object condition checker</h1>
  <!-- Style bind -->
  <h2 v-bind:style="{color:highlightColor,'font-size':headersSize,padding:'20px'}">Inline style</h2>
<h2 v-bind:style="headersSizeObject
">Style object</h2>
<div>
<h1 v-bind:style="[baseStyleObject,successStyleObject]">Success Style</h1>
</div>
  </div>

</template>

<script>
export default {
  data() {
    return {
      greet: "Hello",
      message: "<b>Welcome to Vue.js</b>",
      channel: "Vue.js",
      headingId: "heading",
      isDisabled: false,
      status: "danger",
      isPromoted: true,
      isSoldOut: true,
      highlightColor: "orange",
      headersSize:"50px",
      headersSizeObject:{ color:"red", fontSize:"20px", padding:"10px" },
      baseStyleObject:{ color:"blue", fontSize:"20px", padding:"10px" },
      successStyleObject:{ backgroundColor:"lightgreen", border:'1px solid green', }

     
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
.uderline {
  text-decoration: underline;
}
.promoted {
  text-transform: uppercase;
}
.new {
  color: red;
}
.sold-out {
  color: green;
}
</style>
