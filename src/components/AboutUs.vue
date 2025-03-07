<template>
    <section class="about-us">
      <h2>Chi Siamo</h2>
      <div class="about-content">
        <div class="image-container">
          <!-- Immagine clown rotonda -->
          <img src="../assets/images/about-img.jpg" alt="Clown Round" />
        </div>
        <div class="about-text">
          <p>
            Siamo un team di clown appassionati di programmazione. Offriamo corsi
            online interattivi e divertenti, con certificazioni riconosciute.
          </p>
          <ul>
            <li>Formazione di qualità</li>
            <li>Docenti esperti</li>
            <li>Supporto costante</li>
          </ul>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: "AboutUs"
  };
  </script>
  
  <style lang="scss" scoped>
  @import '../assets/styles/variables.scss';

  .about-us {
    background-color: white;
    padding: 2rem;
    text-align: center;
    h2 {
      font-size: 1.8rem;
      margin-bottom: 1rem;
      color: $primary-color;
    }
    .about-content {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 2rem;
      margin-top: 2rem;
  
      .image-container {
        img {
          border-radius: 50%;
        }
      }
      .about-text {
        color:black ;
        max-width: 500px;
        text-align: left;
        p {
          margin-bottom: 1rem;
        }
        ul {
          list-style: none;
          li {
            
            margin: 0.5rem 0;
          }
        }
      }
    }
  
    @media (max-width: 768px) {
      .about-content {
        flex-direction: column;
        text-align: center;
        .about-text {
          text-align: center;
        }
      }
    }
  }
  </style>
  