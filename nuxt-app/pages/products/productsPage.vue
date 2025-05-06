<template>
  <div>
    <h2>Products Page</h2>

    <!-- make a card -->
    <div v-for="product in products" :key="product.id">
      <img :src="product.image" alt="">
      {{ product.title }}
     R{{ product.price }}
      {{ product.description }} 

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

// getAllProducts
const {data: products} = await useFetch('https://fakestoreapi.com/products')


</script>
<style>

</style>

