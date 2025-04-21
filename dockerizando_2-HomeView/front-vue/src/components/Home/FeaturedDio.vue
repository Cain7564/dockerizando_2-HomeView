<template>
    <section class="figures-section">
      <h2>Figuras y Dioramas</h2>
      <div class="figures-grid">
        <div class="figure-card" v-for="(figure, index) in figures" :key="index">
          <h3>{{ figure.name }}</h3>
          <p class="stock">{{ figure.stock }}</p>
          <p class="price">{{ figure.price }} GTQ</p>
          <button class="add-to-cart">Añadir al carrito</button>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'FiguresSection',
    data() {
      return {
        figures: [
          { name: 'Figura Dragon Ball Z', price: '420.00', stock: 'EN STOCK' },
          { name: 'Diorama Attack on Titan', price: '550.00', stock: 'EN STOCK' },
          { name: 'Figura One Piece - Luffy', price: '380.00', stock: 'EN STOCK' }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .figures-section {
    margin: 50px 0;
  }
  
  .figures-section h2 {
    color: #333;
    margin-bottom: 20px;
    font-size: 24px;
    border-bottom: 2px solid #780116;
    padding-bottom: 10px;
  }
  
  .figures-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 20px;
  }
  
  .figure-card {
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
    .figures-grid {
      grid-template-columns: 1fr 1fr;
    }
  }
  
  @media (max-width: 480px) {
    .figures-grid {
      grid-template-columns: 1fr;
    }
  }
  </style>