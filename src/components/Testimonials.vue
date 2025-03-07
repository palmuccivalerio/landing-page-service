<template>
  <section class="testimonials">
    <h2>Recensioni</h2>
    <ReviewSlider />
  </section>
</template>

<script>
import ReviewSlider from './ReviewSlider.vue';

export default {
  name: "Testimonials",
  components: { ReviewSlider }
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.testimonials {
  text-align: center;
  padding: 2rem;
  background-color: bg-color;

  h2 {
    font-size: 1.8rem;
    color: $primary-color;
    margin-bottom: 2rem;
  }
}
</style>
