<template>
  <WordBox />
</template>

<script>
import WordBox from './components/WordBox.vue'

export default {
  name: 'App',
  components: {
    WordBox
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
