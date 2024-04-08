<script>
export default {
    name: 'SectionOurProducts'
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
                <i class="fa-solid fa-chevron-left"></i>
                <i class="fa-solid fa-chevron-right"></i>
                <div class="card">
                    <img src="/img/choco-chip-cookies-400x510.jpg" alt="choco-chip-cookies">
                    <div class="info">
                        <div class="name">Choco Chip Cookies</div>
                        <div class="category">Cookies, Patries</div>
                        <div class="prices">
                            <span>$19.00</span>
                            <span>$39.00</span>
                        </div>
                    </div>
                </div>
                <div class="card">
                    <img src="/img/strawberry-jam-cookies-400x510.jpg" alt="strawberry-jam-cookies">
                    <div class="info">
                        <div class="name">Choco Chip Cookies</div>
                        <div class="category">Cookies, Patries</div>
                        <div class="prices">
                            <span>$19.00</span>
                            <span>$39.00</span>
                        </div>
                    </div>
                </div>
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
