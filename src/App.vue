<template>
  <div id="app">
    <Navigation/>
  </div>
</template>

<script>
import Navigation from "./components/Navigation";

export default {
  name: "App",
  components: {
    Navigation
  }
};
</script>

<style>
  #app { 
    height: 100%;
  }
  
  html, body {
    padding: 0;
    margin: 0;
    height: 100%;
  }
</style>
