<template>
  <div>
    <h1>{{ title }}<a href='https://toolio-retail.myshopify.com/' target="_blank" rel="noopener">{{ link }}</a></h1>
    <form class="mt-5">
      <div class="row">
        <div class="form-group col-8">
          <input type="text" class="form-control form-control-lg" placeholder="Type anything to filter a product..." autofocus>
        </div>
        <div class="form-group col-4 d-grid gap-2">
          <button type="submit" class="btn btn-primary" @click.prevent="$emit('filterProducts', searchParam, $event)">Filter Results</button>
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
      searchParam: '',
      title: 'Filter Products for ',
      link: 'Toolio Shopify Account'
    }
  }
}
</script>