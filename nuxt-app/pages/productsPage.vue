<template>
  <div>
    <h2>Products Page</h2>

    <!-- make a card -->
    <div v-for="product in products" :key="product.id">
      <p>Here are the products: {{ product.title }} {{ product.id }}  </p>
      <img :src="product.image" alt="">
    
    
    
    </div>






</div>
</template>

<script setup>


/*
UPDATES
useFetch() -> automatic handling of SSR
           -> automatic handling reactivity
           -> automatic json parsing


use (useFetch instead of fetch)

currently using fetch() -> manual handling SSR
                        -> manually parse response to .json 
                        -> !reactive

Steps
1 -> change from fetch(url) to useFetch url for auto handling of json parsing and SSR
*/

// get
const {data: products} = await useFetch('https://fakestoreapi.com/products')


</script>
<style>
</style>

