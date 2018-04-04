<template>
  <section class="section">
    <div class="left">
      <div class="line"></div>
    </div>

    <div class="right">
      <h1 class="title"><slot name="title"></slot></h1>

      <Item 
        v-for="item in items" 
        :range="item.range" 
        :title="item.title" 
        :subtitle="item.subtitle" 
        :text="item.text"
        :key="item.range"
      />
    </div>
  </section>
</template>

<script>
import Item from "./Item";

export default {
  name: "Section",
  props: ['items'],
  components: {
    Item
  }
};
</script>

<style lang="scss" scoped>
.section {
  display: flex;
  align-items: stretch;
}

.left {
  flex: 0 0 50px;
  display: flex;
  justify-content: center;
  padding-top: 40px;
}

.right {
  flex: 1;
}

.line {
  width: 2px;
  height: 100%;
  background-color: black;
}

.title {
  font-size: 18px;
  font-variant: small-caps;
  border-bottom: 2px solid black;
  padding-bottom: 14px;
  font-weight: normal;
  letter-spacing: 6px;
  text-transform: uppercase;
}
</style>
