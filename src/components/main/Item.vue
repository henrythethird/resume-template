<template>
  <div class="item">
    <div class="year">2012-2014</div>
    <div class="description">
      <div class="item-title">PwC AG - Digital Services</div>
      <div class="item-subtitle">Junior Software Engineer</div>
      <div class="item-text">Sartorial cardigan flexitarian health goth. Flannel swag synth man braid, drinking vinegar gastropub neutra. Gastropub yr drinking vinegar hell of pug viral irony vape cold-pressed scenester cronut whatever woke VHS brunch. Try-hard locavore vice gluten-free wolf. Chicharrones skateboard man braid, woke pinterest yr microdosing. Microdosing sriracha selfies VHS glossier shabby chic YOLO jianbing beard put a bird on it activated charcoal drinking vinegar cornhole roof party flannel.</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Item'
}
</script>

<style lang="scss" scoped>
  .item {
    position: relative;

    &::before {
      position: absolute;
      top: 0;
      left: -10px;
      display: block;

      content: "";
      width: 5px;
      height: 5px;
      border-radius: 100%;
      background-color: black;
    }
  }
</style>

