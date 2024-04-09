<script>
export default {
    name: 'SectionShop',
    props: {
        images: Array
    },
    data() {
        return {
            active: [0, 1, 2, 3],
        }
    },
    methods: {
        prev() {
            if (this.active[0] > 0) {
                this.active[0]--;
                this.active[1]--;
                this.active[2]--;
                this.active[3]--;
            } else {
                this.active[0] = this.images.length - 4;
                this.active[1] = this.images.length - 3;
                this.active[2] = this.images.length - 2;
                this.active[3] = this.images.length - 1;
            }
        },
        next() {
            if (this.active[3] < this.images.length - 1) {
                this.active[0]++;
                this.active[1]++;
                this.active[2]++;
                this.active[3]++;
            } else {
                this.active = [0, 1, 2, 3]
            }
        }
    }
}
</script>

<template>
    <!-- shop products -->
    <section class="shop">
        <div class="container">
            <div class="section_text">
                <h3>Find a freshly baked product perfect for you</h3>
                <p>
                    Sit amet consectetur elit. Fuga tempore
                    assumenda facere dolores exercitationem commodi impedit.
                </p>
                <button class="btn-negative">Shop All Products</button>
            </div>
            <div class="carousel">
                <!-- arrows control -->
                <i @click="prev" class="fa-solid fa-chevron-left"></i>
                <i @click="next" class="fa-solid fa-chevron-right"></i>
                <!-- cards -->
                <template v-for="(image, index) in images" :key="image.name">
                    <div v-if="active.includes(index)" class="card">
                        <img :src="image.src" alt="choco-chip-cookies">
                        <div class="info">
                            <div class="name">{{ image.name }}</div>
                            <div class="prices">
                                <span>${{ image.price.min }} - ${{ image.price.max }}</span>
                            </div>
                        </div>
                    </div>
                </template>
            </div>
        </div>
    </section>
</template>

<style>
section.shop {

    .container {
        display: flex;
        align-items: center;

        .section_text {
            width: 30%;
            text-align: center;
            padding: 0 3rem 0 1rem;

            & button {
                margin: auto;
            }
        }

        .carousel {
            width: 70%;
            display: flex;
            height: 355px;
            gap: .5rem;
            position: relative;
            align-items: center;

            .card {
                width: calc(100% / 4);
                height: 100%;
                position: relative;

                & img {
                    width: 100%;
                    height: 80%;
                    display: block;
                    object-fit: cover;
                }

                .info {
                    position: static;
                    color: var(--bake-primary);
                    background-color: transparent;
                    text-align: center;
                    margin-top: .2rem;
                    height: 20%;

                    .name,
                    .prices {
                        line-height: 1rem;
                    }

                    .prices {
                        margin-top: .5rem;

                        & span {
                            margin: 0;
                            color: var(--bake-secondary-dark);
                            font-size: .85rem;
                            font-weight: 500;
                        }
                    }
                }
            }

            & i {
                z-index: 1;
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
}
</style>
