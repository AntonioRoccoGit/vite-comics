<script>
export default {
    name: "AppFooter",
    data() {
        return {
            footerLinks: {
                "dc comics": [
                    "characters",
                    "Comics",
                    "Movies",
                    "TV",
                    "Games",
                    "Videos",
                    "News"
                ],
                "dc": [
                    "Terms of Use",
                    "Privacy policy(New)",
                    "Ad Choices",
                    "Adverstring",
                    "Jobs",
                    "Subscriptions",
                    "Talent Workshops",
                    "CPSC Certificates",
                    "Ratings",
                    "Shop Help",
                    "Contact Us"
                ],
                "sites": [
                    "DC",
                    "MAD Magazine",
                    "DC Kids",
                    "DC Universe",
                    "DC Power Visa"
                ],
                "shop": [
                    "Shop DC",
                    "Shop DC Collectables"
                ]
            },
        }
    }

}
</script>

<template>
    <!-- footer top -->
    <section class="footer-top">
        <div class="container">
            <div class="footer-top-link">
                <div v-for="(item, key) in footerLinks" class="card">
                    <h2>{{ key }}</h2>
                    <ul>
                        <li v-for="link in item"><a href="">{{ link }}</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-top-logo">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </section>
    <!-- /footer top -->

    <!-- footer bottom -->
    <section class="footer-bottom">
        <div class="container">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sapiente, quae deserunt tempore eius adipisci nobis
            officia voluptatum incidunt, vel qui quidem ipsum. Nobis tempora itaque harum fugit est aspernatur quis.

        </div>
    </section>
    <!-- /footer bottom -->
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

.footer-top {
    height: $footer_top_height;
    background-image: url("../assets/img/footer-bg.jpg");
    background-size: auto;
    position: relative;

    &-link {
        width: 450px;
        display: flex;
        flex-wrap: wrap;

        .card {
            width: calc(100% / 3);

            h2 {
                text-transform: uppercase;
                color: white;
                font-size: .6rem;
                margin-top: 1rem;
            }

            ul {
                list-style-type: none;
                padding-top: .4rem;

                a {
                    color: rgba(255, 255, 255, 0.288);
                    text-decoration: none;
                    font-size: .6rem;
                }
            }
        }
    }

    &-logo {
        left: 50%;
        top: -50px;
        position: absolute;
        height: 450px;
        width: 450px;
        z-index: 0;
    }

    .container {
        display: flex;

    }

}

.footer-bottom {
    position: relative;
    background-color: white;
    z-index: 10;
    height: $header_height;
}

img {
    max-width: 100%;
    max-height: 100%;
}
</style>