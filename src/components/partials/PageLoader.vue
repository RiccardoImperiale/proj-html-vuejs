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
    setTimeout(() => {
      this.isLoading = false;
    }, 2100);
  },

}
</script>

<template>
  <transition name="loader">
    <div v-if="isLoading" class="loader">
      <img width="260" ref="gif" src="/img/logo.gif" alt="logo gif">
    </div>
  </transition>
  <transition name="oval">
    <div v-if="isLoading" class="oval"></div>
  </transition>
</template>

<style>
.loader-leave-active {
  transition: transform .5s cubic-bezier(0.9, 0, 1, 1);
}

.loader-leave-to {
  transform: translateY(-100%);
}

.oval-enter-active,
.oval-leave-active {
  transition: transform .5s cubic-bezier(0.9, 0, 1, 1);
}

.oval-enter-from {
  transform: translate(-5%, 0) scaleY(1);
}

.oval-leave-to {
  transform: translate(-5%, -100vh) scaleY(0);
}

.loader {
  position: fixed;
  inset: 0;
  background-color: var(--bake-scroll);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 990;
}

.oval {
  position: fixed;
  bottom: -400px;
  width: 110%;
  height: 800px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 900;
  background-color: var(--bake-scroll);
  box-shadow: 0px 200px 100px -50px rgba(92, 92, 92, 0.156);
}
</style>
