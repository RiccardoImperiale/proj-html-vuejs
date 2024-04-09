<script>
export default {
    name: 'AppFooter',
    props: {
        navLinks: Object
    }
}
</script>

<template>
    <footer>
        <div class="container">
            <div class="top">
                <div class="left">
                    <img width="150" src="/img/avada-bakery-logo-retina-200x97.png" alt="logo bakery">
                    <nav>
                        <ul class="nav_links">
                            <li v-for="link in navLinks.footer" :key="link.text"><a href="#">{{ link.text }}</a></li>
                            <li><a href="#"><i class="fa-solid fa-cart-shopping"></i></a></li>
                        </ul>
                        <div class="cart_items_num">0</div>
                    </nav>
                </div>
                <div class="right">
                    <h3>Subscribe to our Newsletter</h3>
                    <div class="subscribe">
                        <input type="text" placeholder="Enter email address*">
                        <button class="btn-negative">Subscribe</button>
                    </div>
                </div>
            </div>
            <div class="bottom">
                <div class="left">
                    <div class="copy">© Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All rights Reserved |
                        Powered by WordPress</div>
                </div>
                <div class="right">
                    <div class="socials">
                        <i class="fa-brands fa-instagram"></i>
                        <i class="fa-brands fa-x-twitter"></i>
                        <i class="fa-brands fa-facebook-f"></i>
                        <i class="fa-brands fa-pinterest-p"></i>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style>
footer {
    height: 400px;

    .container {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        height: 100%;
    }

    .top,
    .bottom {
        display: flex;
        justify-content: space-between;
        padding: 4rem 0;
    }

    & nav {
        margin-top: 2rem;
        display: flex;
        align-items: center;

        .nav_links {
            list-style: none;
            display: flex;
            gap: 2rem;
            text-transform: capitalize;
            font-weight: 300;
            letter-spacing: .05rem;
            font-size: 1rem;

            & li {
                padding: .25rem 0;

                & a {
                    text-decoration: none;
                }
            }

            .fa-cart-shopping {
                font-size: .9rem;
            }
        }

        .cart_items_num {
            background-color: var(--bake-secondary);
            border-radius: 50%;
            width: 22px;
            aspect-ratio: 1;
            margin-left: .4rem;
            font-size: .85rem;
            line-height: 22px;
            text-align: center;
        }
    }

    .bottom {
        align-items: center;
    }

    .right {
        text-align: end;

        .subscribe {
            margin-top: 2rem;
            display: flex;
            gap: 1rem;

            & input {
                width: 310px;
                border: 1px solid var(--bake-secondary);
                border-radius: .3rem;
                padding-left: 1rem;
                outline: none;
            }
        }
    }

    .copy {
        font-size: .6rem;
        color: var(--bake-secondary-dark);
    }

    .socials {
        display: flex;
        gap: 1.8rem;

        & i {
            cursor: pointer;
        }
    }
}
</style>
