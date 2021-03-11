<template>
  <div class="mt-5">
    <h1 class="mb-4">{{ filteredProducts.length > 0 ? filterTitle : title }}</h1>
    <table class="table table-success table-bordered table-striped">
      <thead>
        <th>#</th>
        <th>Product ID</th>
        <th>Product Title</th>
      </thead>
      <tbody>
        <tr v-for="(product, i) in allProducts" :key="i">
          <td>{{ i + 1 }}</td>
          <td>{{ product.id}}</td>
          <td>{{ product.title}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'ResultList',
  data: function() {
    return {
      title: 'All Products:',
      filterTitle: 'Filtered Results:',
      filteredProducts: []
    }
  },
  props: ["allProducts"]
}
</script>