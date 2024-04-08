<script>
import SectionHero from './SectionHero.vue';
import SectionProducts from './SectionProducts.vue';
import SectionMoments from './SectionMoments.vue';
import SectionShop from './SectionShop.vue';

export default {
    name: 'AppMain',
    components: {
        SectionHero,
        SectionProducts,
        SectionMoments,
        SectionShop
    }
}
</script>

<template>
    <main>
        <SectionHero />
        <SectionProducts />
        <SectionMoments />
        <SectionShop />
        <!-- process -->
        <section class="process">
            <div class="container">
                <div class="banner_01">
                    <div class="left">
                        <h2>Tell us what you have in mind</h2>
                    </div>
                    <div class="right">
                        <div class="number">01</div>
                        <div class="text">
                            <h6>manual ingredients selection</h6>
                            <p>
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta molestias similique
                                perspiciatis fugit est nostrum, assumenda quidem tempora praesentium exercitationem
                                officia aspernatur aut quae ipsum at eius harum consequuntur quibusdam!
                            </p>
                        </div>
                    </div>
                </div>
                <div class="banner_02">
                    <div class="left">
                        <h2>We Start Baking</h2>
                        <div class="text">
                            <h6>sweet & delicious</h6>
                            <p>
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta molestias similique
                                perspiciatis fugit est nostrum, assumenda quidem tempora praesentium exercitationem
                                officia aspernatur aut quae ipsum at eius harum consequuntur quibusdam!
                            </p>
                        </div>
                    </div>
                    <div class="right">
                        <div class="number">02</div>
                    </div>
                </div>
                <div class="banner_02b">
                    <div class="section_text">
                        <h6>sweet & delicious</h6>
                        <h2>"Finally foud an alternative to the masss produced products. Something that incorporates
                            real organic ingredients, nutrient dense wellness while promoting sustainability and
                            activity."</h2>
                        <h6>Rachel Cooper, Founder</h6>
                    </div>
                </div>
                <div class="banner_03">
                    <div class="left">
                        <h2>Delivered to you home</h2>
                        <div class="text">
                            <h6>manual ingredients selection</h6>
                            <p>
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta molestias similique
                                perspiciatis fugit est nostrum, assumenda quidem tempora praesentium exercitationem
                                officia aspernatur aut quae ipsum at eius harum consequuntur quibusdam!
                            </p>
                        </div>
                    </div>
                    <div class="right">
                        <div class="number">03</div>
                    </div>
                </div>
            </div>
        </section>
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

section.process {
    .container {
        display: flex;
        flex-wrap: wrap;
        gap: 1.2rem;
    }

    .banner_01,
    .banner_03 {
        aspect-ratio: 2/1;
    }

    .banner_02 {
        aspect-ratio: 1;
    }

    .banner_01,
    .banner_02,
    .banner_03 {
        position: relative;
        background-size: cover;
        background-position: center;
        /* height: 500px; */
        padding: 4rem;
        z-index: -1;
        display: flex;
        color: var(--bake-light);

        &::after {
            content: '';
            position: absolute;
            inset: 0;
            background-color: rgba(39, 39, 39, 0.5);
            z-index: -1;
        }

        .left,
        .right {
            width: 50%;
        }

        .left {
            padding-right: 10rem;

            & h2 {
                color: var(--bake-light);
                font-size: 2.2rem;
            }
        }

        .right {
            .text {
                padding-right: 1rem;
                margin-bottom: 2rem;
            }

            .number {
                text-align: end;
                font-size: 3.8rem;
                font-weight: 100;
            }
        }

        .text {
            & h6 {
                text-transform: uppercase;
                font-weight: 200;
                margin-bottom: .8rem;
            }

            & p {
                font-size: .8rem;
                line-height: 1.2rem;
            }
        }
    }

    .banner_02,
    .banner_02b {
        width: calc(50% - 0.7rem);
    }

    .banner_01 {
        background-image: url("/img/bakery-process-1.jpg");

        .right {
            padding-left: 6rem;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }
    }

    .banner_02 {
        background-image: url("/img/bakery-process-2.jpg");

        .right {
            width: 20%;
        }

        .left {
            width: 80%;
            padding-right: 1rem;
            display: flex;
            flex-direction: column;
            justify-content: space-between;

            .text {
                margin-bottom: 2rem;
            }
        }
    }

    .banner_02b {
        background-color: var(--bake-secondary);
        padding: 3rem;
        display: flex;
        align-items: center;

        & h2 {
            font-size: 2rem;
            line-height: 2.6rem;
        }

        & h6:last-child {
            text-transform: none;
        }
    }

    .banner_03 {
        background-image: url("/img/bakery-process-3.jpg");

        .left {
            display: flex;
            flex-direction: column;
            justify-content: space-between;

            .text {
                margin-bottom: 2rem;
            }
        }

    }

}
</style>
