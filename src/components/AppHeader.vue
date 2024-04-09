<script>
export default {
    name: 'AppHeader',
    props: {
        navLinks: Object
    },
    data() {
        return {
            isTransparent: true,
            isHidden: false,
            isWhite: false,
            scrollPosition: 0
        };
    },
    mounted() {
        window.addEventListener('scroll', () => {
            const scroll = window.scrollY;
            if (scroll > 600) {
                if (scroll > this.scrollPosition) {
                    this.isHidden = true;
                    this.isWhite = true;
                    this.isTransparent = false;
                } else {
                    this.isHidden = false;
                }
            } else if (scroll > 30) {
                if (scroll > this.scrollPosition) {
                    this.isHidden = false;
                    this.isWhite = true;
                } else {
                    this.isTransparent = false;
                }
            } else {
                this.isHidden = false;
                this.isWhite = false;
                this.isTransparent = true;
            }
            this.scrollPosition = scroll;
        });
    }
}
</script>

<template>
    <header :class="{ 'transparent': isTransparent, 'hidden': isHidden, 'white_bg': isWhite }">
        <nav>
            <img width="150" src="/img/avada-bakery-logo-retina-200x97.png" alt="logo bakery">
            <ul class="nav_links">
                <li v-for="link in navLinks.header" :key="link.text"><a href="#">{{ link.text }}</a></li>
                <li><a href="#"><i class="fa-solid fa-cart-shopping"></i></a></li>
            </ul>
        </nav>
    </header>
</template>

<style>
header {
    padding: .8rem 2rem;
    position: fixed;
    width: 100%;
    z-index: 100;
    transition: background-color 0.5s ease, transform 0.25s ease;
    border-bottom: 1px solid var(--bake-secondary);
    transform: translateY(0);

    &.transparent {
        background-color: transparent;
    }

    &.hidden {
        transform: translateY(-100%);
    }

    &.white_bg {
        background-color: var(--bake-light);
    }

    & nav {
        display: flex;
        justify-content: space-between;
        align-items: center;

        & img {
            margin-top: -0.5rem;
        }

        .nav_links {
            list-style: none;
            display: flex;
            gap: 1.6rem;
            text-transform: uppercase;
            font-weight: 500;
            letter-spacing: .05rem;
            font-size: .75rem;

            & li {
                padding: .25rem 0;

                & a {
                    text-decoration: none;
                }
            }

            & li:first-child {
                border-bottom: 2px solid var(--bake-primary);
            }

            .fa-cart-shopping {
                font-size: .8rem;
            }
        }
    }
}
</style>
