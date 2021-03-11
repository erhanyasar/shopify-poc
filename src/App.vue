<template>
  <div id="app">
    <div class="container">
      <FormInput />
      <ResultList />
      <ProductService />
    </div>
  </div>
</template>

<script>
import FormInput from './components/FormInput.vue'
import ResultList from './components/ResultList.vue'
import ProductService from './utils/product.service.vue'

export default {
  name: 'App',
  components: {
    FormInput,
    ResultList,
    ProductService
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
