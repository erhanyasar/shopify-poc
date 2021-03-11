<template>
  <div class="container">
    <h1>Filter Products for <a href="https://toolio-retail.myshopify.com/" target="_blank" rel="noopener">Toolio Shopify Account</a></h1>
    <form class="mt-5">
      <div class="row">
        <div class="form-group col-8">
          <input type="text" class="form-control form-control-lg" placeholder="Type anything to filter a product...">
        </div>
        <div class="form-group col-4 d-grid gap-2">
          <button type="submit" class="btn btn-primary">Submit</button>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
import '../../node_modules/bootstrap/dist/css/bootstrap.min.css';

export default {
  name: 'FormInput'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>