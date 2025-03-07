<template>
  <section class="hero">
    <div class="hero-text">
      <h1>Impara a Programmare con i Migliori Clown</h1>
      <p>Oltre 100+ corsi, 500+ docenti, tutto completamente GRATIS!</p>
      <div class="highlights">
        <div class="highlight-box">100+ Corsi</div>
        <div class="highlight-box">500+ Docenti</div>
        <div class="highlight-box">GRATIS!</div>
      </div>
      <button class="cta">Inizia ora</button>
    </div>
    <div class="hero-image">
      <!-- Sostituisci con la tua immagine clown -->
      <img src="../assets/images/billboard-img.png" alt="Clown" />
    </div>
  </section>
</template>

<script>
export default {
  name: "Hero"
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 2rem;
  background-color: #fff;

  .hero-text {
    flex: 1;
    margin-right: 1rem;
    h1 {
      font-size: 2rem;
      margin-bottom: 1rem;
      color: $primary-color;
      font-weight: 600;
    }
    p {
      font-weight: 300;
      margin-bottom: 1rem;
    }
    .highlights {
      display: flex;
      gap: 1rem;
      margin: 1rem 0;
      .highlight-box {
        background-color: $secondary-color;
        color: #fff;
        padding: 0.5rem 1rem;
        border-radius: 4px;
        font-weight: 600;
      }
    }
    .cta {
      background-color: $primary-color;
      color: #fff;
      padding: 0.75rem 1.5rem;
      border: none;
      cursor: pointer;
      &:hover {
        background-color: darken($primary-color, 10%);
      }
    }
  }

  .hero-image {
    flex: 1;
    text-align: right;
    img {
      border-radius: 8px;
      max-width: 100%;
      height: auto;
    }
  }

  @media (max-width: 768px) {
    flex-direction: column;
    .hero-text {
      margin-right: 0;
      text-align: center;
      margin-bottom: 1.5rem;
    }
    .hero-image {
      text-align: center;
    }
  }
}
</style>
