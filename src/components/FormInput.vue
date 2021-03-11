<template>
  <div id="form-input" class="container">
    <h1>{{ title }}<a href='https://toolio-retail.myshopify.com/' target="_blank" rel="noopener">{{ link }}</a></h1>
    <form class="mt-5">
      <div class="row">
        <div class="form-group col-8">
          <input type="text" v-model="searchParam" class="form-control form-control-lg" placeholder="Type anything to filter a product...">
        </div>
        <div class="form-group col-4 d-grid gap-2">
          <button type="submit" class="btn btn-primary">Filter Results</button>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'FormInput',
  data: function() {
    return {
      title: 'Filter Products for ',
      link: 'Toolio Shopify Account'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>