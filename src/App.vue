<template>
  <div id="app">
    <!-- HEADER -->
    <upperHeader/>
  </div>
</template>

<script>
import upperHeader from './components/upperHeader.vue'

export default {
  name: 'App',
  components: {
    upperHeader,
  }
}
</script>

<style lang="scss">
@import './assets/commons.scss';
</style>
