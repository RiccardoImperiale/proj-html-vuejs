<script>
import SectionHero from './SectionHero.vue';

export default {
    name: 'AppMain',
    components: {
        SectionHero
    },
    props: {
        navLinks: Array
    }
}
</script>

<template>
    <main>
        <SectionHero />
        <!-- products -->
        <section class="products">
            <div class="container">
                <div class="section_text">
                    <h6>our products</h6>
                    <h3>All our delectable pastries are baked fresh in our Kitchen each morning, and are made with
                        all-natural, all organic ingredients.</h3>
                    <button class="btn-negative">Start Shopping</button>
                </div>
                <div class="carousel">
                    <i class="fa-solid fa-chevron-left"></i>
                    <i class="fa-solid fa-chevron-right"></i>
                    <div class="image">
                        <img src="/img/choco-chip-cookies-400x510.jpg" alt="choco-chip-cookies">
                    </div>
                    <div class="image">
                        <img src="/img/strawberry-jam-cookies-400x510.jpg" alt="strawberry-jam-cookies">
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<style>
section.products {
    padding: 8rem 0;

    .container {
        display: flex;
    }

    .section_text {
        width: 40%;
        padding-right: 5rem;
    }

    .carousel {
        width: 60%;
        display: flex;
        height: 510px;
        gap: 1rem;
        position: relative;
        align-items: center;

        .image {
            width: 50%;
            height: 100%;

            & img {
                width: 100%;
                height: 100%;
                display: block;
                object-fit: cover;
            }
        }

        & i {
            position: absolute;
            background-color: var(--bake-primary-light);
            padding: 1.4rem .6rem;
            cursor: pointer;
            color: var(--bake-secondary);
            transition: background-color .25s ease;

            &:hover {
                background-color: var(--bake-primary);
            }
        }

        .fa-chevron-left {
            left: 0;
        }

        .fa-chevron-right {
            right: 0;
        }

    }
}
</style>
