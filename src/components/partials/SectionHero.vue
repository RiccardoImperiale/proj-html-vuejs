<script>
export default {
    name: 'SectionHero'
}
</script>

<template>
    <!-- hero -->
    <section class="hero">
        <div class="container">
            <div class="badges">
                <div class="badge">
                    <img src="/img/demo-icon.png" alt="fewf">
                    <span>Demos</span>
                </div>
                <div class="badge">
                    <div class="price">
                        <i class="fa-solid fa-dollar-sign"></i>
                        <h3>39</h3>
                    </div>
                    <span>Demos</span>
                </div>
            </div>
            <div class="section_text">
                <h6>fresh & tasty bakery every day</h6>
                <h2>The Perfect Fresh Bread</h2>
                <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quod quaerat tempore officiis corporis
                    possimus ut
                    animi doloribus placeat labore sequi quasi cum quis.
                </p>
                <button>Explore our products</button>
            </div>
        </div>
    </section>
</template>

<style>
section.hero {
    height: 680px;
    background-image: url("/img/hero-header-bakery.jpg");
    background-size: cover;
    background-position: center;
    display: flex;
    position: relative;
    top: 0;
    width: 100%;

    .section_text {
        width: 400px;
    }

    .badges {
        position: absolute;
        top: 8rem;
        right: .6rem;

        .badge {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: var(--bake-light);
            color: var(--bake-secondary-dark);
            width: 50px;
            aspect-ratio: 1;
            border-radius: .3rem;
            margin-bottom: .5rem;
            font-size: 1rem;
            box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.184);
            gap: .2rem;
            cursor: pointer;

            & img {
                margin-bottom: -0.2rem;
                width: 25px;
            }

            & span {
                font-size: .6rem;
                letter-spacing: 0;
                font-weight: 500;
            }

            .price {
                display: flex;
                color: rgb(74, 197, 74);

                & h3 {
                    line-height: 1rem;
                    font-family: var(--ff-noto-sans);
                }

                .fa-dollar-sign {
                    font-size: .6rem;
                }
            }
        }
    }
}
</style>
