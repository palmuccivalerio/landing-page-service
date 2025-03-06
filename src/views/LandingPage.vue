<!-- src/views/LandingPage.vue -->
<template>
    <div class="landing-page">
      <Header />
      <Hero />
      <Testimonials />
      <Footer />
    </div>
  </template>
  
  <script>
  import Header from '../components/Header.vue';
  import Hero from '../components/Hero.vue';
  import Testimonials from '../components/Testimonials.vue';
  import Footer from '../components/Footer.vue';
  
  export default {
    name: "LandingPage",
    components: {
      Header,
      Hero,
      Testimonials,
      Footer,
    },
  };
  </script>
  
  <style lang="scss" scoped>
  @import '../assets/styles/global.scss';
  
  .landing-page {
    font-family: 'Inter', sans-serif;
    background-color: #E2F3F0;
    min-height: 100vh; /* 100% dell'altezza della viewport */
  width: 100%;
  }
  </style>
  