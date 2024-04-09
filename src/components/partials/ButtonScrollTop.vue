<script>
export default {
    name: 'ButtonScrollTop',
    data() {
        return {
            isScrollTopBtn: false
        }
    },
    mounted() {
        window.addEventListener('scroll', () => {
            window.scrollY >= 800 ? this.isScrollTopBtn = true : this.isScrollTopBtn = false;
        });
    },
    methods: {
        scrollToTop() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        }
    }
}
</script>

<template>
    <transition name="scrollButton">
        <button v-if="isScrollTopBtn" @click="scrollToTop" class="scroll_top_btn">
            <i class="fa-solid fa-angle-up"></i>
        </button>
    </transition>
</template>

<style>
.scrollButton-enter-active,
.scrollButton-leave-active {
    transition: opacity .25s ease;
}

.scrollButton-enter,
.scrollButton-leave-to {
    opacity: 0;
}

.scroll_top_btn {
    position: fixed;
    bottom: 2rem;
    right: 2rem;
    width: 40px;
    padding: 0;
    aspect-ratio: 1;
    background-color: var(--bake-secondary-dark);
    color: var(--bake-light);
    z-index: 3;
}
</style>
