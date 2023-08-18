<template>
  <HeroComp/>
  <h1>INSERT SOME COOL TEXT</h1>
  <HomePageProductsDisplay/>
  <h3>View All Products</h3>
</template>

<script>
import HeroComp from '../components/HeroComp.vue'
import HomePageProductsDisplay from '../components/HomePageProductsDisplay.vue'

export default {
  name: 'HomeView',
  components: {
    HeroComp,
    HomePageProductsDisplay
  }
}
</script>

<style scoped>
*{
  color: white;
}
</style>