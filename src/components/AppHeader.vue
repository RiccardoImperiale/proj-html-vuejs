<script>
export default {
  name: 'AppHeader',
  props: {
    navLinks: Array
  },
  data() {
    return {

    }
  }
}
</script>

<template>
  <header>
    <nav>
      <img width="150" src="/img/avada-bakery-logo-retina-200x97.png" alt="logo bakery">
      <ul class="nav_links">
        <li v-for="link in navLinks" :key="link.text"><a href="#">{{ link.text }}</a></li>
        <li><a href="#"><i class="fa-solid fa-cart-shopping"></i></a></li>
      </ul>
    </nav>
  </header>
</template>

<style>
header {
  padding: 1rem 2rem;
  position: absolute;
  width: 100%;
  z-index: 1;

  & nav {
    display: flex;
    justify-content: space-between;
    align-items: center;

    .nav_links {
      list-style: none;
      display: flex;
      gap: 1.6rem;
      text-transform: uppercase;
      font-weight: 500;
      letter-spacing: .05rem;
      font-size: .75rem;

      & li {
        padding: .25rem 0;

        & a {
          text-decoration: none;
        }
      }

      & li:first-child {
        border-bottom: 2px solid var(--bake-primary);
      }

      .fa-cart-shopping {
        font-size: .8rem;
      }
    }
  }
}
</style>
