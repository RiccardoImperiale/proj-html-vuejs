<script>
export default {
    name: 'SectionShop'
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
                <i class="fa-solid fa-chevron-left"></i>
                <i class="fa-solid fa-chevron-right"></i>
                <!-- cards -->
                <div class="card">
                    <img src="/img/choco-chip-cookies-400x510.jpg" alt="choco-chip-cookies">
                    <div class="info">
                        <div class="name">Choco Chip Cookies</div>
                        <div class="prices">
                            <span>$19.00 - $39.00</span>
                        </div>
                    </div>
                </div>
                <div class="card">
                    <img src="/img/strawberry-jam-cookies-400x510.jpg" alt="strawberry-jam-cookies">
                    <div class="info">
                        <div class="name">Strawberry Jam Cookies</div>
                        <div class="prices">
                            <span>$19.00 - $39.00</span>
                        </div>
                    </div>
                </div>
                <div class="card">
                    <img src="/img/strawberry-jam-cookies-400x510.jpg" alt="strawberry-jam-cookies">
                    <div class="info">
                        <div class="name">Strawberry Jam Cookies</div>
                        <div class="prices">
                            <span>$19.00 - $39.00</span>
                        </div>
                    </div>
                </div>
                <div class="card">
                    <img src="/img/strawberry-jam-cookies-400x510.jpg" alt="strawberry-jam-cookies">
                    <div class="info">
                        <div class="name">Strawberry Jam Cookies</div>
                        <div class="prices">
                            <span>$19.00 - $39.00</span>
                        </div>
                    </div>
                </div>
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
