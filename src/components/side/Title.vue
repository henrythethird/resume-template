<template>
  <h1 class="title"><slot>Replace this title</slot></h1>
</template>

<script>
export default {
  name: 'Title'
}
</script>

<style lang="scss" scoped>
  .title {
    font-size: 18px;
    font-variant: small-caps;
    color: white;
    border-bottom: 2px solid white;
    padding-bottom: 14px;
    font-weight: normal;
    letter-spacing: 6px;
    text-transform: uppercase;
  }
</style>

