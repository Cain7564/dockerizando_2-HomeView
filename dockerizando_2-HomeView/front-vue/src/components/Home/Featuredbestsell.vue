<template>
    <section class="categories-section">
      <h2>Categorías Especiales</h2>
      <div class="category-grid">
        <div class="category-card" v-for="(category, index) in categories" :key="index">
          <h3>{{ category.name }}</h3>
          <p class="stock">{{ category.stock }}</p>
          <p class="price">{{ category.price }}</p>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'SpecialCategories',
    data() {
      return {
        categories: [
          { name: 'Máscaras y Accesorios', stock: 'IN STOCK', price: '$27.00' },
          { name: 'Colleccionables y Decoración', stock: 'IN STOCK', price: '$22.00' },
          { name: 'Merchandising', stock: 'IN STOCK', price: '$43.00' }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .categories-section {
    margin: 50px 0;
  }
  
  .categories-section h2 {
    color: #333;
    margin-bottom: 20px;
    font-size: 24px;
    border-bottom: 2px solid #780116;
    padding-bottom: 10px;
  }
  
  .category-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 20px;
  }
  
  .category-card {
    border: 1px solid #eee;
    border-radius: 8px;
    padding: 15px;
    text-align: center;
  }
  
  .price {
    color: #780116;
    font-weight: bold;
    font-size: 18px;
    margin: 10px 0;
  }
  
  .stock {
    color: #4CAF50;
    font-weight: 500;
  }
  
  @media (max-width: 768px) {
    .category-grid {
      grid-template-columns: 1fr 1fr;
    }
  }
  
  @media (max-width: 480px) {
    .category-grid {
      grid-template-columns: 1fr;
    }
  }
  </style>