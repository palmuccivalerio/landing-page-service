<template>
    <section class="popular-categories">
      <h2>Categorie Popolari</h2>
      <div class="categories-grid">
        <div class="category-box" v-for="(category, index) in categories" :key="index">
          {{ category }}
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: "PopularCategories",
    data() {
      return {
        categories: ["Front-end", "Back-end", "Design", "UI/UX", "Data Science", "Security"]
      };
    }
  };
  </script>
  
  <style lang="scss" scoped>
  @import '../assets/styles/variables.scss';
  
  .popular-categories {
    padding: 2rem;
    text-align: center;
    h2 {
      font-size: 1.8rem;
      margin-bottom: 1.5rem;
      color: $primary-color;
    }
    .categories-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 1rem;
      .category-box {
        background-color: $secondary-color;
        color: #fff;
        padding: 1rem;
        border-radius: 4px;
        font-weight: 600;
      }
      @media (min-width: 768px) {
        grid-template-columns: repeat(3, 1fr);
      }
    }
  }
  </style>
  