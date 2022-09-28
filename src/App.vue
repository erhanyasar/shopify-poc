<template>
  <div id="main-app" class="container">
    <form-input @filter="filterProducts"/>
    <result-list :allProducts="allProducts"/>
  </div>
</template>

<script>
  import axios from 'axios';
  import FormInput from './components/FormInput.vue'
  import ResultList from './components/ResultList.vue'

  export default {
    name: 'MainApp',
    components: {
      FormInput,
      ResultList
    },
    data: function() {
      return {
        allProducts: []
      }
    },
    mounted() {
      axios
        .get("./products.json")
        .then(response => {
          this.allProducts = response.data.products
        });
    },
    methods: {
      filterProducts: function(searchParam, event) {
        alert(event.target.payload[0]);
      }
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