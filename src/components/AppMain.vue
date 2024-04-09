<script>
import SectionHero from './partials/SectionHero.vue';
import SectionProducts from './partials/SectionProducts.vue';
import SectionMoments from './partials/SectionMoments.vue';
import SectionShop from './partials/SectionShop.vue';
import SectionProcess from './partials/SectionProcess.vue';
import SectionLocations from './partials/SectionLocations.vue';
import SectionSocial from './partials/SectionSocial.vue';
import ButtonScrollTop from './partials/ButtonScrollTop.vue';
import AppBanner from './AppBanner.vue';

export default {
    name: 'AppMain',
    components: {
        SectionHero,
        SectionProducts,
        SectionMoments,
        SectionShop,
        SectionProcess,
        SectionLocations,
        SectionSocial,
        AppBanner,
        ButtonScrollTop
    },

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
        <SectionSocial />
        <AppBanner />

        <ButtonScrollTop />

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
