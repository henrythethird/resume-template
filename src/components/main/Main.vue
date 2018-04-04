<template>
  <div class="main">
    <h1 class="name">{{ name }}</h1>
    <h2 class="position">Software Engineering Student</h2>

    <Section><template slot="title">work experience</template></Section>
  </div>
</template>

<script>
import Section from './Section'

export default {
  name: 'Main',
  props: ['name'],
  components: {
    Section
  }
}
</script>

<style lang="scss" scoped>
  .name {
    padding: 0;
    margin-top: 20px;
    font-size: 50px;
  }

  .position {
    font-size: 16px;
    font-style: italic;
    opacity: 0.6;
    letter-spacing: 3px;
    font-variant: small-caps;
    margin-bottom: 124px;
  }

  .main {
    padding: 50px;
  }
</style>