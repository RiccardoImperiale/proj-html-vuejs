<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import PageLoader from './components/partials/PageLoader.vue';
import ButtonScrollTop from './components/partials/ButtonScrollTop.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    PageLoader,
    ButtonScrollTop
  },
  data() {
    return {
      navLinks: {
        header: [
          { href: '#', text: 'home' },
          { href: '#', text: 'shop' },
          { href: '#', text: 'about' },
          { href: '#', text: 'gallery' },
          { href: '#', text: 'locations' },
          { href: '#', text: 'journal' },
          { href: '#', text: 'contact' },
          { href: '#', text: 'my account' },
        ],
        footer: [
          { href: '#', text: 'shop' },
          { href: '#', text: 'about' },
          { href: '#', text: 'gallery' },
          { href: '#', text: 'locations' },
          { href: '#', text: 'journal' },
          { href: '#', text: 'contact' },
          { href: '#', text: 'orders' },
        ]
      }
    }
  }
}
</script>

<template>
  <PageLoader />
  <AppHeader :navLinks="navLinks" />
  <AppMain />
  <ButtonScrollTop />
  <AppFooter :navLinks="navLinks" />
</template>

<style></style>
