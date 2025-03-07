<template>
  <footer class="footer">
    <p>&copy; 2025 CODECIRCUS - Tutti i diritti riservati</p>
  </footer>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.footer {
  text-align: center;
  padding: 1rem;
  background-color: $primary-color;
  color: #fff;
}
</style>
