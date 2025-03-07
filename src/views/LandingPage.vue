<template>
  <div class="landing-page">
    <Header />
    <Hero />
    <AboutUs />
    <PopularCategories />
    <ExploreCourses />
    <Testimonials />
    <Footer />
  </div>
</template>

<script>
import Header from '../components/Header.vue';
import Hero from '../components/Hero.vue';
import AboutUs from '../components/AboutUs.vue';
import PopularCategories from '../components/PopularCategories.vue';
import ExploreCourses from '../components/ExploreCourses.vue';
import Testimonials from '../components/Testimonials.vue';
import Footer from '../components/Footer.vue';

export default {
  name: "LandingPage",
  components: {
    Header,
    Hero,
    AboutUs,
    PopularCategories,
    ExploreCourses,
    Testimonials,
    Footer
  }
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/global.scss';

.landing-page {

  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
</style>
