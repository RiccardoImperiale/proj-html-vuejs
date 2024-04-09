<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter
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
  <AppHeader :navLinks="navLinks" />
  <AppMain />
  <AppFooter :navLinks="navLinks" />
</template>

<style></style>
