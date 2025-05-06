<template>
    <div>
        <h2> Product details {{ id }}</h2>

        <img :src="product.image" alt="">
    </div>
</template>

<script setup>
import {useRoute} from 'vue-router'
const route = useRoute()
const id = route.params.id
</script>

<style  scoped>

</style>