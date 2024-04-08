<script>
import AppHeader from './components/AppHeader.vue'
export default {
  name: 'App',
  components: {
    AppHeader
  },
  data() {
    return {
      navLinks: [
        { href: '#', text: 'home' },
        { href: '#', text: 'shop' },
        { href: '#', text: 'about' },
        { href: '#', text: 'gallery' },
        { href: '#', text: 'locations' },
        { href: '#', text: 'journal' },
        { href: '#', text: 'contact' },
        { href: '#', text: 'my account' },
      ]
    }
  }
}
</script>

<template>
  <AppHeader :navLinks="navLinks" />
  <section class="hero">
    <div class="container">
      <div class="hero_text">
        <h6>fresh & tasty bakery every day</h6>
        <h2>The Perfect Fresh Bread</h2>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quod quaerat tempore officiis corporis possimus ut
          animi doloribus placeat labore sequi quasi cum quis.
        </p>
        <button>Explore our products</button>
      </div>
    </div>
  </section>
</template>

<style>
.container {
  width: 85%;
  max-width: 1440px;
  margin: auto;
}

button {
  background-color: var(--bake-light);
  padding: .8rem 1.8rem;
  color: var(--bake-primary);
  border: none;
  border-radius: .5rem;
  font-size: .92rem;
  cursor: pointer;
  transition: all .25s ease;

  &:hover {
    background-color: var(--bake-primary);
    color: var(--bake-light);
  }
}


section.hero {
  height: 680px;
  background-image: url("/img/hero-header-bakery.jpg");
  background-size: cover;
  background-position: center;
  display: flex;
  position: absolute;
  top: 0;
  width: 100%;
  z-index: -1;

  .hero_text {
    width: 450px;
    display: flex;
    flex-direction: column;
    gap: 1.2rem;

    & h6 {
      text-transform: uppercase;
      color: var(--bake-secondary-dark);
      font-weight: 400;
    }

    & h2 {
      font-size: 2.8rem;
      line-height: 3.2rem;
      font-family: "Noto Serif", serif;
      letter-spacing: 0;
    }

    & p {
      color: var(--bake-secondary-dark);
      font-weight: 300;
      font-size: .9rem;
      line-height: 1.5rem;
    }

    & button {
      margin-right: auto;
    }
  }
}
</style>
