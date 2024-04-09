<script>
export default {
    name: 'SectionProducts',
    data() {
        return {
            active: [0, 1],
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
        };
    },
    methods: {
        prev() {
            if (this.active[0] > 0) {
                this.active[0]--;
                this.active[1]--;
            } else {
                this.active[0] = this.images.length - 2;
                this.active[1] = this.images.length - 1;
            }
        },
        next() {
            if (this.active[1] < this.images.length - 1) {
                this.active[0]++;
                this.active[1]++;
            } else {
                this.active[0] = 0;
                this.active[1] = 1;
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
                    <div v-if="active[0] === index" class="card">
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
                    <div v-if="active[1] === index" class="card">
                        <img :src="image.src" alt="strawberry-jam-cookies">
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
