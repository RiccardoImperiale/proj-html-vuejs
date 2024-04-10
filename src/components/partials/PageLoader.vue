<script>
export default {
  name: 'PageLoader',
  data() {
    return {
      isLoading: true,
    }
  },
  mounted() {
    // restart the gif 
    window.addEventListener('load', () => {
      const gif = this.$refs.gif;
      gif.src = gif.src;
    });
    // stop the page loader 
    setTimeout(() => {
      this.isLoading = false;
    }, 2100);
  },
}
</script>

<template>
  <transition>
    <div v-if="isLoading" class="loader">
      <img width="300" ref="gif" src="/img/logo.gif" alt="logo gif">
    </div>
  </transition>
</template>

<style>
.v-leave-active {
  transition: transform .5s cubic-bezier(0.9, 0, 1, 1);
}

.v-leave-to {
  transform: translateY(-100%);
}

.loader {
  position: fixed;
  inset: 0;
  background-color: var(--bake-scroll);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 900;
}
</style>
