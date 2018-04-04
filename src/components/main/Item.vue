<template>
  <div class="item">
    <div class="year">{{ range }}</div>
    <div class="description">
      <div class="title">{{ title }}</div>
      <div class="subtitle">{{ subtitle }}</div>
      <div class="text">{{ text }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Item',
  props: ['range', 'title', 'subtitle', 'text']
}
</script>

<style lang="scss" scoped>
  .item {
    margin-top: 20px;
    display: flex;

    position: relative;

    &::before {
      position: absolute;
      top: 4px;
      left: -30px;
      display: block;

      content: "";
      width: 6px;
      height: 6px;
      border-radius: 100%;
      background-color: white;
      border: 2px solid black;
    }
  }

  .year {
    flex: 0 0 100px;
    font-size: 14px;
    opacity: 0.7;
  }

  .title {
    font-weight: bold;
  }

  .subtitle {
    opacity: 0.7;
    font-size: 14px;
    font-style: italic;
    margin-bottom: 8px;
  }

  .text {
    font-size: 13px;
  }
</style>

