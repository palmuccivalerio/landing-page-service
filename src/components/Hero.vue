<!-- src/components/Hero.vue -->
<template>
  <section class="hero">
    <h1>Scopri i nostri corsi online</h1>
    <p>Impara nuove competenze con i migliori esperti</p>
    <button class="cta-button">Inizia ora</button>
  </section>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.hero {
  text-align: center;
  padding: 40px 20px;
  background-color: white;

  h1 {
    font-size: 28px;
    color: $primary-color;
    font-weight: 600;
    margin-bottom: 20px;
    /* Fluid typography: aumentare il font su schermi più grandi */
    @media (min-width: 768px) {
      font-size: 36px;
    }
  }

  p {
    font-size: 16px;
    font-weight: 300;
    margin-bottom: 20px;
    @media (min-width: 768px) {
      font-size: 18px;
    }
  }

  .cta-button {
    background-color: $secondary-color;
    color: white;
    padding: 10px 20px;
    border: none;
    cursor: pointer;
    transition: background-color 0.3s ease;
    
    &:hover {
      background-color: darken($secondary-color, 10%);
    }
  }
}
</style>
