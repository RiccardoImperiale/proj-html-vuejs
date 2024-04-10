<script>
import SectionHero from './partials/SectionHero.vue';
import SectionProducts from './partials/SectionProducts.vue';
import SectionMoments from './partials/SectionMoments.vue';
import SectionShop from './partials/SectionShop.vue';
import SectionProcess from './partials/SectionProcess.vue';
import SectionLocations from './partials/SectionLocations.vue';
import SectionSocial from './partials/SectionSocial.vue';
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
    },
    data() {
        return {
            images: [
                { src: '/img/choco-chip-cookies-400x510.jpg', name: 'Choco Chip Cookies', category: 'Cookies, Patries', price: { min: '19.00', max: '39.00' }, },
                { src: '/img/strawberry-jam-cookies-400x510.jpg', name: 'Strawberry Jam Cookies', category: 'Cookies, Patries', price: { min: '19.00', max: '39.00' }, },
                { src: '/img/cherry-cake-400x510.jpg', name: 'Cherry Cake', category: 'Cakes', price: { min: '21.00', max: '49.00' }, },
                { src: '/img/cookies-with-ice-cream-400x510.jpg', name: 'Cookies With Ice Cream', category: 'Ice Cream', price: { min: '8.00', max: '12.00' }, },
                { src: '/img/perfect-macarons-400x510.jpg', name: 'Perfect Macarons', category: 'Cookies, Patries', price: { min: '14.00', max: '41.00' }, },
                { src: '/img/blackberry-stuffed-bread-400x510.jpg', name: 'Blackberry Stuffed Bread', category: 'Bread, Patries', price: { min: '11.00', max: '31.00' }, },
                { src: '/img/glazed-pancake-with-lemon-400x510.jpg', name: 'Glazed Pancake With Lemon', category: 'Cakes, Patries', price: { min: '12.00', max: '32.00' }, },
                { src: '/img/home-bread-400x510.jpg', name: 'Home Bread', category: 'Bread, Patries', price: { min: '9.00', max: '11.00' }, },
            ],
        }
    }
}
</script>

<template>
    <main>
        <SectionHero />
        <SectionProducts :images="images" />
        <SectionMoments />
        <SectionShop :images="images" />
        <SectionProcess />
        <SectionLocations />
        <SectionSocial />
        <AppBanner />
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
                font-family: var(--ff-source);
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
