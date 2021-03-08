<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <FormInput />
    <ResultList />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import FormInput from './components/FormInput.vue'
import ResultList from './components/ResultList.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    FormInput,
    ResultList
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
