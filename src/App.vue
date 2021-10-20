<template>
  <div id="app">
    <counter-interface />
  </div>
</template>

<script>
import CounterInterface from './components/CounterInterface.vue'

export default {
  name: 'App',
  components: {
    CounterInterface
  }
}
</script>

<style lang="scss">
@import './assets/global-styles';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: $dark-violet;
  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: column;
  align-content: center;
  justify-content: center;
}
</style>
