<template>
    <div>
      <header>
        <Header />
      </header>
  
      <main>
        <HeroSlider />
        <FeaturedCategories />
        <FeaturedThemes />
        <FeaturedProducts />
      </main>
  
    </div>
  </template>
  
  <script setup>
  import Header from '@/components/Header.vue'
  import HeroSlider from '@/components/Home/HeroSlider.vue'
  import FeaturedCategories from '@/components/Home/FeaturedCategories.vue'
  import FeaturedThemes from '@/components/Home/FeaturedThemes.vue'
  import FeaturedProducts from '@/components/Home/FeaturedProducts.vue'
  import Featuredbestseell from '@/components/Home/Featuredbestseell.vue'
  import FeaturedSpecial from '@/components/Home/FeaturedSpecial.vue'
  import Featureddio from '@/components/Home/FeaturedDio
  
  
  .vue'
  </script>
  
  <style scoped>
  main {
    display: flex;
    flex-direction: column;
    gap: 40px;
  }
  </style>
  