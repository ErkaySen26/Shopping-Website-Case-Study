<template>
  <div id="app">
    <Header />
    <ProductDetails />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import ProductDetails from '@/components/ProductDetails.vue'

export default {
  name: 'App',
  components: {
    Header,
    ProductDetails
  }
}
</script>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}
</style>
