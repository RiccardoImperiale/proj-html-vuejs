<script>
export default {
    name: 'SectionProducts',
    props: {
        images: Array
    },
    data() {
        return {
            active: [0, 1],
        };
    },
    methods: {
        prev() {
            if (this.active[0] > 0) {
                this.active[0]--;
                this.active[1]--;
            } else {
                this.active = [this.images.length - 2, this.images.length - 1];
            }
        },
        next() {
            if (this.active[1] < this.images.length - 1) {
                this.active[0]++;
                this.active[1]++;
            } else {
                this.active = [0, 1];
            }
        }
    }
}
</script>

<template>
    <!-- products -->
    <section class="our_products">
        <div class="container">
            <div class="section_text">
                <h6>our products</h6>
                <h3>All our delectable pastries are baked fresh in our Kitchen each morning, and are made with
                    all-natural, all organic ingredients.</h3>
                <button class="btn-negative">Start Shopping</button>
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
                            <div class="category">{{ image.category }}</div>
                            <div class="prices">
                                <span>${{ image.price.min }}</span>
                                <span>${{ image.price.max }}</span>
                            </div>
                        </div>
                    </div>
                </template>
            </div>
        </div>
    </section>
</template>

<style>
section.our_products {
    .container {
        display: flex;
    }

    .section_text {
        width: 40%;
        padding-right: 5rem;

        & h3 {
            margin-bottom: 1.6rem;
        }
    }

    .carousel {
        width: 60%;
        display: flex;
        height: 510px;
        gap: 1rem;
        position: relative;
        align-items: center;

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
</style>
