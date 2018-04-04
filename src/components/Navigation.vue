<template>
  <nav class="navigation">
    <div class="picture-wrapper">
      <Picture class="pic" />
    </div>
    <p>Hello</p>
  </nav>
</template>

<script>
import Picture from './Picture'

export default {
  name: "HelloWorld",
  components: {
    Picture
  },
  data() {
    return {
      msg: "Welcome to Your Vue.js App"
    };
  }
};
</script>

<style scoped lang="scss">
  .navigation {
    width: 300px;
    height: 100%;
    background-color: #222222;

    display: flex;
    flex-direction: column;
  }

  .picture-wrapper {
    flex-basis: 100%;
    display: flex;
    justify-content: center;
    padding: 50px;
  }
</style>
