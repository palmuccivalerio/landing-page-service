<template>
    <swiper :slides-per-view="1" :loop="true" class="review-slider" pagination="true">
      <swiper-slide v-for="(review, index) in reviews" :key="index">
        <div class="review-card">
          <img :src="review.img" :alt="review.author" />
          <p>{{ review.text }}</p>
          <h4>{{ review.author }}</h4>
        </div>
      </swiper-slide>
    </swiper>
  </template>
  
  <script>
  import { Swiper, SwiperSlide } from 'swiper/vue';
  import 'swiper/swiper-bundle.css';
  
  export default {
    name: "ReviewSlider",
    components: {
      Swiper,
      SwiperSlide
    },
    data() {
      return {
        reviews: [
          {
            img: "../assets/images/reviwer1.jpg",
            text: "Corso davvero ben fatto, ho imparato tantissimo!",
            author: "Mario Rossi"
          },
          {
            img: "../assets/images/reviwer2.jpg",
            text: "Docenti preparati e grande disponibilità!",
            author: "Luca Bianchi"
          },
          {
            img: "../assets/images/reviwer3.jpg",
            text: "Le lezioni sono divertenti e interattive!",
            author: "Giulia Verdi"
          }
        ]
      };
    }
  };
  </script>
  
  <style lang="scss" scoped>
  .review-slider {
    padding: 2rem;
    .review-card {
      background-color: #fff;
      border-radius: 8px;
      text-align: center;
      padding: 2rem;
      max-width: 400px;
      margin: 0 auto;
      img {
        border-radius: 50%;
        margin-bottom: 1rem;
      }
      p {
        margin-bottom: 1rem;
        font-weight: 300;
      }
      h4 {
        font-weight: 600;
        color: #333;
      }
    }
  }
  </style>
  