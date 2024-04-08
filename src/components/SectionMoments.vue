<script>
export default {
    name: 'SectionMoments'
}
</script>

<template>
    <!-- moments -->
    <section class="moments">
        <div class="container">
            <div class="section_text">
                <h6>corporate & weddings</h6>
                <h3>Baking Special Moments</h3>
            </div>
            <div class="section_images">
                <div class="card">
                    <img src="/img/corporate-bg.jpg" alt="corporate">
                    <div class="info">
                        <img src="/img/corporate-hover-bg.jpg" alt="corporate">
                        <div class="info">
                            <img src="/img/wedding-hover-bg.jpg" alt="wedding cake">
                            <div class="section_text">
                                <h6>international bakery</h6>
                                <h3>Corporate Events</h3>
                                <button class="btn-negative">Explore More</button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="card">
                    <img src="/img/wedding-bg.jpg" alt="wedding">
                    <div class="info">
                        <img src="/img/wedding-hover-bg.jpg" alt="wedding cake">
                        <div class="section_text">
                            <h6>private dining hall</h6>
                            <h3>Weddings & Parties</h3>
                            <button class="btn-negative">Explore More</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style>
section.moments {

    .container {
        display: flex;
        justify-content: center;
        text-align: center;
        flex-direction: column;
    }

    .section_images {
        display: flex;
        gap: 4rem;
        margin-top: 1.4rem;

        .section_text {
            position: absolute;

            & h6 {
                text-transform: uppercase;
                color: var(--bake-light);
                font-weight: 400;
            }

            & h3 {
                margin-bottom: 0;
            }

            & button {
                margin: auto;
            }
        }
    }



}
</style>
