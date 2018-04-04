<template>
  <div id="app">
    <Side class="nav" />
    <Main class="main" :name="'Long Johnson'"/>
  </div>
</template>

<script>
import Side from "./components/side/Side";
import Main from "./components/main/Main";

export default {
  name: "App",
  components: {
    Side,
    Main
  }
};
</script>

<style>
  #app { 
    height: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: stretch;
  }

  html, body {
    height: 100%;
  }

  * {
    font-family: Arial, sans-serif;
    font-size: inherit;
    padding: 0;
    margin: 0;
  }

  .nav {
    flex-basis: 300px;
  }

  .main {
    flex: 1;
  }
</style>
