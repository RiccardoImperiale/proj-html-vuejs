<script>
import SectionHero from './SectionHero.vue';
import SectionProducts from './SectionProducts.vue';
import SectionMoments from './SectionMoments.vue';
import SectionShop from './SectionShop.vue';
import SectionProcess from './SectionProcess.vue';
import SectionLocations from './SectionLocations.vue';

export default {
    name: 'AppMain',
    components: {
        SectionHero,
        SectionProducts,
        SectionMoments,
        SectionShop,
        SectionProcess,
        SectionLocations
    }
}
</script>

<template>
    <main>
        <SectionHero />
        <SectionProducts />
        <SectionMoments />
        <SectionShop />
        <SectionProcess />
        <SectionLocations />

    </main>
</template>

<style>
section {
    padding-top: 8rem;

    .card {
        width: 50%;
        height: 100%;
        position: relative;

        &:hover .info {
            opacity: 1;
        }

        & img {
            width: 100%;
            height: 100%;
            display: block;
            object-fit: cover;
        }

        .info {
            display: flex;
            opacity: 0;
            align-items: center;
            flex-direction: column;
            justify-content: center;
            position: absolute;
            background-color: rgba(37, 37, 37, 0.399);
            inset: 0;
            width: 100%;
            height: 100%;
            color: var(--bake-light);
            transition: opacity .25s ease;

            .name {
                font-family: var(--ff-noto-serif);
                font-weight: 700;
                letter-spacing: 0;
            }

            .category {
                font-size: .6rem;
            }

            .prices {
                margin-top: .8rem;

                & span {
                    margin: 0 .5rem;
                }
            }
        }
    }
}
</style>
