<template>
    <section class="explore-courses">
      <h2>Esplora i Corsi Online</h2>
      <div class="courses-grid">
        <div class="course-card" v-for="(course, index) in courses" :key="index">
          <img :src="course.img" :alt="course.title" />
          <h3>{{ course.title }}</h3>
          <p>{{ course.description }}</p>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: "ExploreCourses",
    data() {
      return {
        courses: [
          {
            img: "https://via.placeholder.com/300x200/FFFFFF/000000?text=Corso+1",
            title: "Corso 1",
            description: "Introduzione alla programmazione front-end."
          },
          {
            img: "https://via.placeholder.com/300x200/FFFFFF/000000?text=Corso+2",
            title: "Corso 2",
            description: "Sviluppo di API e microservizi."
          },
          {
            img: "https://via.placeholder.com/300x200/FFFFFF/000000?text=Corso+3",
            title: "Corso 3",
            description: "UX/UI Design e prototipazione."
          },
          {
            img: "https://via.placeholder.com/300x200/FFFFFF/000000?text=Corso+4",
            title: "Corso 4",
            description: "Sicurezza informatica e best practice."
          }
        ]
      };
    }
  };
  </script>
  
  <style lang="scss" scoped>
  @import '../assets/styles/variables.scss';
  
  .explore-courses {
    padding: 2rem;
    text-align: center;
  
    h2 {
      font-size: 1.8rem;
      margin-bottom: 2rem;
      color: $primary-color;
    }
  
    .courses-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 1.5rem;
      .course-card {
        background-color: #fff;
        border-radius: 8px;
        padding: 1rem;
        text-align: left;
        margin: 0 auto;
        max-width: 300px;
        img {
          border-radius: 8px;
          margin-bottom: 1rem;
        }
        h3 {
          margin: 0.5rem 0;
          color: $primary-color;
        }
      }
      @media (min-width: 768px) {
        grid-template-columns: repeat(4, 1fr);
        .course-card {
          max-width: 100%;
        }
      }
    }
  }
  </style>
  