<template>
  <div id="app">
    <HeadComp />
    <MainComp />
  </div>
</template>

<script>
import HeadComp from './components/HeadComp.vue'
import MainComp from './components/MainComp.vue'

export default {
  name: 'App',
  components: {
    HeadComp,
    MainComp
  }
}
</script>

<style lang="scss">
#app {
  height: 100vh;
}
</style>
