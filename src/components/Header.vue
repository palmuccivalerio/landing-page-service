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
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      isMenuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    }
  }
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.header {
  background-color: $primary-color;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;

  .logo {
    color: #fff;
    font-weight: 600;
    font-size: 1.5rem;
  }

  .mobile-menu-toggle {
    display: none;
    background: none;
    border: none;
    font-size: 1.5rem;
    color: #fff;
    cursor: pointer;
  }

  .menu {
    ul {
      display: flex;
      gap: 1.5rem;
      list-style: none;
      li a {
        color: #fff;
        text-decoration: none;
        &:hover {
          color: lighten($primary-color, 20%);
        }
      }
    }
    &.open {
      /* Per mobile, quando aperto */
    }
  }

  @media (max-width: 768px) {
    .mobile-menu-toggle {
      display: block;
    }
    .menu {
      display: none;
      position: absolute;
      top: 60px;
      left: 0;
      width: 100%;
      background-color: $primary-color;
      ul {
        flex-direction: column;
        text-align: center;
        padding: 1rem 0;
      }
      &.open {
        display: block;
      }
    }
  }
}
</style>
