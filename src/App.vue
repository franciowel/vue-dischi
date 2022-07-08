<template>
  <div id="app">
  
  <header>
    <upperHeader/>
  </header>

  <main>
    <MainContent/>
  </main>
  </div>
</template>

<script>
import upperHeader from './components/upperHeader.vue'
import MainContent from './components/MainContent.vue'

export default {
  name: 'App',
  components: {
    upperHeader,
    MainContent,
  }
}
</script>

<style lang="scss">
@import './assets/commons.scss';
</style>
