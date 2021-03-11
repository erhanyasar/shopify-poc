<template>
  <div id="main-app" class="container">
    <FormInput />
    <ResultList />
    <ProductService />
  </div>
</template>

<script>
import FormInput from './components/FormInput.vue'
import ResultList from './components/ResultList.vue'
import ProductService from './utils/product.service.vue'

export default {
  name: 'MainApp',
  components: {
    FormInput,
    ResultList,
    ProductService
  }
}
</script>

<style>
#main-app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
