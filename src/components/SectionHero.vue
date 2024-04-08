<script>
export default {
    name: 'SectionHero'
}
</script>

<template>
    <main>
        <!-- hero -->
        <section class="hero">
            <div class="container">
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
    </main>
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
}
</style>
