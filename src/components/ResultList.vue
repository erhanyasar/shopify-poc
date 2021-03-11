<template>
  <div id="result-list" class="container mt-5">
    <h1>{{ filteredProducts.length > 0 ? filterTitle : title }}</h1>
    <table class="table table-success table-bordered table-striped">
      <thead>
        <th>#</th>
        <th>Product ID</th>
        <th>Product Title</th>
      </thead>
      <tbody>
        <tr v-for="(product, i) in filteredProducts" :key="i">
          <td>{{ i + 1 }}</td>
          <td>{{ product.id}}</td>
          <td>{{ product.title}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'ResultList',
  data: function() {
    return {
      title: 'All Products:',
      filterTitle: 'Filtered Results:',
      filteredProducts: []
    }
  },
  mounted() {
    axios.get("./products.json")
      .then(response => {
        //console.log(response.data.products);
        this.filteredProducts = response.data.products
      });
  }
}
</script>