<script>
export default {
    name: 'AppBanner'
}
</script>

<template>
    <!-- banner -->
    <div class="call_to_action">
        <div class="container-sm">
            <!-- <img src="/img/call-to-action-bg.jpg" alt=""> -->
            <div class="section_text">
                <h6>try our seasonal products</h6>
                <h3>Order for pick-up or delivery to your home</h3>
                <button>Shop Now</button>
            </div>
        </div>
    </div>
</template>

<style>
.call_to_action {
    margin-top: 6rem;
    height: 400px;
    background-image: url("/img/call-to-action-bg.jpg");
    background-size: cover;

    .container-sm {
        position: relative;
        display: flex;
        align-items: center;
        height: 100%;

        .section_text {
            position: absolute;
            width: 600px;

            & h3,
            h6 {
                color: var(--bake-light);
            }

            & h6 {
                opacity: .6;
            }

            & h3 {
                font-size: 2.2rem;
                line-height: 2.8rem;
                margin-bottom: 1.6rem;
            }
        }
    }
}
</style>
