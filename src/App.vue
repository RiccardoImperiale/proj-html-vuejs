<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
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
  <AppMain />

</template>

<style></style>
