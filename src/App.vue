<template>
  <div id="app">
    <QuestionOne/>
  </div>
</template>

<script>
import QuestionOne from './components/QuestionOne.vue'

export default {
  name: 'app',
  components: {
    QuestionOne
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
