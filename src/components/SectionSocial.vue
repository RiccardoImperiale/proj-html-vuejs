<script>
export default {
    name: 'SectionSocial'
}
</script>

<template>
    <!-- social -->
    <section class="social">
        <div class="container">
            <div class="cards">
                <div class="row">
                    <img class="square" src="/img/social-1.jpg" alt="">
                    <div class="banner">
                        <div class="section_text">
                            <h6>made for sharing</h6>
                            <h3>Let's stay in touch</h3>
                            <button class="btn-negative"><i class="fa-brands fa-instagram"></i> Follow Us</button>
                        </div>
                    </div>
                    <img class="square" src="/img/social-2.jpg" alt="">
                </div>
                <div class="row">
                    <img class="square" src="/img/social-3.jpg" alt="">
                    <img class="square" src="/img/social-4.jpg" alt="">
                    <img class="square" src="/img/social-5.jpg" alt="">
                    <img class="square" src="/img/social-6.jpg" alt="">
                </div>

            </div>
        </div>
    </section>
</template>

<style>
section.social {

    .cards {

        .row {
            display: flex;
            margin: 0 -10px;
        }

        .row:first-child {
            margin-bottom: 20px;
        }

        .square {
            width: calc(25% - 20px);
            margin: 0 10px;
            aspect-ratio: 1;
            object-fit: cover;
        }

        .banner {
            width: calc(50% - 20px);
            margin: 0 10px;
            background-color: var(--bake-secondary);
            display: flex;
            align-items: center;
            justify-content: center;

            .section_text {
                text-align: center;

                & button {
                    margin: auto;

                    &:hover {
                        background-color: var(--bake-light);
                    }
                }
            }
        }
    }
}
</style>
