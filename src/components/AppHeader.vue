<script>
export default {
  name: 'AppHeader',
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
        <li><a href="#">home</a></li>
        <li><a href="#">shop</a></li>
        <li><a href="#">about</a></li>
        <li><a href="#">gallery</a></li>
        <li><a href="#">locations</a></li>
        <li><a href="#">journal</a></li>
        <li><a href="#">contact</a></li>
        <li><a href="#">my account</a></li>
        <li><a href="#"><i class="fa-solid fa-cart-shopping"></i></a></li>
      </ul>
    </nav>
  </header>
</template>

<style>
header {
  padding: 1rem 2rem;

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
      font-size: .7rem;

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
        margin-left: .5rem;
      }
    }
  }
}
</style>
