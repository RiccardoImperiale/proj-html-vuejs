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
            isWhite: false
        };
    },
    mounted() {
        window.addEventListener('scroll', () => {
            const scroll = window.scrollY;
            if (scroll > 600) {
                this.isHidden = true;
                this.isTransparent = false;
                this.isWhite = true;
            } else if (scroll > 30) {
                this.isHidden = false;
                this.isTransparent = false;
                this.isWhite = true;
            } else {
                this.isTransparent = true;
                this.isHidden = false;
                this.isWhite = false;
            }
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
    z-index: 1;
    transition: background-color 0.5s, opacity 0.25s;

    &.transparent {
        background-color: transparent;
    }

    &.hidden {
        opacity: 0;
        pointer-events: none;
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
