<template>
  <div id="app">
    <HeaderDC></HeaderDC>
  </div>
</template>

<script>
import HeaderDC from './components/HeaderDC.vue'

export default {
  name: 'App',
  components: {
    HeaderDC
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
@import "./assets/styles/style.scss"
</style>
