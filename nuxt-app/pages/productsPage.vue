<template>
  <div>
    <h2>Products Page</h2>
    <div v-for="product in products" :key="product.id">
      <p>here are the products {{ product.title }}</p>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const products = ref([])

async function getProducts(url) {
  const response = await fetch(url)
  products.value = await response.json()
}

onMounted(() => {
  getProducts('https://fakestoreapi.com/products')
})
</script>

<style>
</style>