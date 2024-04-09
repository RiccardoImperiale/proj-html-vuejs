<script>
export default {
    name: 'SectionLocations'
}
</script>

<template>
    <!-- locations -->
    <section class="locations">
        <div class="container">
            <div class="section_text">
                <h6>locations</h6>
                <h3>Visit our Bakery</h3>
            </div>
            <div class="locations">
                <div class="card">
                    <div class="image">
                        <img src="/img/new-york-bk-800x530.jpg" alt="new york bakery">
                    </div>
                    <div class="infos new_york">
                        <div class="left">
                            <div class="bottom">
                                <h6>CALL US</h6>
                                <h6>1.800.458.556</h6>
                            </div>
                        </div>
                        <div class="middle">
                            <h3>New York</h3>
                            <div class="bottom">
                                <h6>OPEN ALL WEEK</h6>
                                <h6>9:00 AM - 6:00 PM</h6>
                            </div>
                        </div>
                        <div class="right">
                            <button>View Map</button>
                        </div>
                    </div>
                </div>
                <div class="card">
                    <div class="image">
                        <img src="/img/london-bk-800x530.jpg" alt="london bakery">
                    </div>
                    <div class="infos london">
                        <div class="left">
                            <div class="bottom">
                                <h6>CALL US</h6>
                                <h6>1.800.458.556</h6>
                            </div>
                        </div>
                        <div class="middle">
                            <h3>London</h3>
                            <div class="bottom">
                                <h6>OPEN ALL WEEK</h6>
                                <h6>9:00 AM - 6:00 PM</h6>
                            </div>
                        </div>
                        <div class="right">
                            <button>View Map</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style>
section.locations {
    .section_text {
        align-items: center;
    }

    .locations {
        margin-top: 1.4rem;
        display: flex;

        .card {
            width: 50%;
        }

        .infos {
            padding: 2rem 3rem;
            display: flex;
            justify-content: space-between;
            align-items: flex-end;
            text-align: center;
            gap: 1rem;

            & h3 {
                text-align: center;
                justify-content: center;
                margin-bottom: 1rem;
                font-size: 1.8rem;
            }

            .bottom {
                height: 40px;
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                padding: .15rem 0;

                & h6 {
                    color: var(--bake-secondary-dark);
                    font-weight: 400;
                    font-size: .8rem;
                }
            }
        }

        .infos.new_york {
            background-color: var(--bake-location-1);
        }

        .infos.london {
            background-color: var(--bake-location-2);
        }
    }
}
</style>
