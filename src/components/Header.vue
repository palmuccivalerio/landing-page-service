<!-- src/components/Header.vue -->
<template>
  <header class="header">
    <div class="logo">CODECIRCUS</div>
    <button class="mobile-menu-toggle" @click="toggleMenu">☰</button>
    <nav class="menu" :class="{ open: isMenuOpen }">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Corsi</a></li>
        <li><a href="#">Contatti</a></li>
      </ul>
    </nav>
    <div class="social-icons">

    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      isMenuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
  },
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: $primary-color;

  .logo {
    font-size: 24px;
    font-weight: 600;
    color: white;
  }

  .menu {
    ul {
      display: flex;
      gap: 20px;
      list-style: none;
      padding: 0;
      margin: 0;
    }
    a {
      color: white;
      text-decoration: none;
      transition: color 0.3s;
      &:hover {
        color: lighten($primary-color, 10%);
      }
    }
    /* Per mobile, il menu sarà nascosto di default */
    @media (max-width: 768px) {
      display: none;
      &.open {
        display: block;
        position: absolute;
        top: 70px;
        left: 0;
        width: 100%;
        background-color: $primary-color;
        ul {
          flex-direction: column;
          text-align: center;
        }
      }
    }
  }

  .mobile-menu-toggle {
    display: none;
    background: none;
    border: none;
    font-size: 24px;
    color: white;
    cursor: pointer;
    @media (max-width: 768px) {
      display: block;
    }
  }

  .social-icons {
    a img {
      width: 24px;
      height: 24px;
      transition: opacity 0.3s;
      &:hover {
        opacity: 0.7;
      }
    }
  }
}
</style>
