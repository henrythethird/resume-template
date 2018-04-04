<template>
  <div class="info-table">
    <Title><slot name="title">Replace me</slot></Title>

    <div class="infos">
      <div v-for="info in infos" :key="info.name" class="info">
        <div class="icon">{{ info.icon }}</div>

        <div class="description">
          <div class="name">{{ info.title }}</div>
          <div class="subtitle">{{ info.subtitle }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Title from './Title'

export default {
  name: 'InfoTable',
  props: ['infos'],
  components: {
    Title
  }
}
</script>

<style lang="scss" scoped>
  .info-table {
    color: white;
    margin: 0 0 20px 50px;
  }

  .infos {
    margin-top: 15px;
  }

  .info {
    display: flex;
    padding: 5px 0;
  }

  .icon {
    flex: 0 0 40px;
    margin-right: 10px;
  }

  .name {
    font-size: 14px;
  }

  .subtitle {
    font-size: 13px;
    opacity: 0.6;
    font-style: italic;
    white-space: pre-wrap;
  }
</style>

