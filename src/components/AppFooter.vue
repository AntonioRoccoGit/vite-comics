<script>
export default {
    name: "AppFooter",
    data() {
        return {
            footerLinks: {
                "dc comics": [
                    {
                        name: "characters",
                        url: "#"
                    },
                    {
                        name: "Comics",
                        url: "#"
                    },
                    {
                        name: "Movies",
                        url: "#"
                    },
                    {
                        name: "TV",
                        url: "#"
                    },
                    {
                        name: "Games",
                        url: "#"
                    },
                    {
                        name: "Videos",
                        url: "#"
                    },
                    {
                        name: "News",
                        url: "#"
                    },

                ],
                "dc": [
                    {
                        name: "Terms of Use",
                        url: "#"
                    },
                    {
                        name: "Privacy policy(New)",
                        url: "#"
                    },
                    {
                        name: "Ad Choices",
                        url: "#"
                    },
                    {
                        name: "Adverstring",
                        url: "#"
                    },
                    {
                        name: "Jobs",
                        url: "#"
                    },
                    {
                        name: "CPSC Certificates",
                        url: "#"
                    },
                    {
                        name: "Subscriptions",
                        url: "#"
                    },
                    {
                        name: "Talent Workshops",
                        url: "#"
                    },
                    {
                        name: "Ratings",
                        url: "#"
                    },
                    {
                        name: "Shop Help",
                        url: "#"
                    },
                    {
                        name: "Contact Us",
                        url: "#"
                    },
                ],
                "sites": [
                    {
                        name: "DC",
                        url: "#"
                    },
                    {
                        name: "MAD Magazine",
                        url: "#"
                    },
                    {
                        name: "DC Kids",
                        url: "#"
                    },
                    {
                        name: "DC Universe",
                        url: "#"
                    },
                    {
                        name: "DC Power Visa",
                        url: "#"
                    },
                ],
                "shop": [
                    {
                        name: "Shop DC",
                        url: "#"
                    },
                    {
                        name: "Shop DC Collectables",
                        url: "#"
                    },
                ]
            },
            socialImg: [
                {
                    img: "footer-facebook.png",
                    url: "https://it-it.facebook.com"
                },
                {
                    img: "footer-twitter.png",
                    url: "https://twitter.com/?lang=it"
                },
                {
                    img: "footer-youtube.png",
                    url: "https://www.youtube.com"
                },
                {
                    img: "footer-pinterest.png",
                    url: "https://www.pinterest.it"
                },
                {
                    img: "footer-periscope.png",
                    url: "#"
                },
            ]
        }
    },
    methods: {
        getImgPath(name) {

            return new URL(`../assets/img/${name.img}`, import.meta.url).href;
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
                        <li v-for="link in item"><a :href="link.url">{{ link.name }}</a></li>
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
            <button>SIGN-UP NOW!</button>
            <ul>
                <li><a href="">FOLLOW US</a></li>
                <li v-for="item in socialImg">
                    <a :href="item.url">
                        <img :src="getImgPath(item)" alt="">
                    </a>
                </li>
            </ul>
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
    background-color: $dark_bg_color;
    z-index: 10;
    height: $footer_bottom_height;

    .container {
        height: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;

        button {
            color: white;
            background-color: inherit;
            border: none;
            padding: .8rem .6rem;
            border: 1px solid $primary_blue;
            cursor: pointer;
        }

        ul {
            display: flex;
            list-style-type: none;

            li {
                &:first-child {
                    font-size: .7rem;
                    font-weight: 600;
                }

                line-height: $footer_bottom_height;
                margin-right: 1rem;
            }

            a {
                text-decoration: none;
                color: $primary_blue;

                img {
                    vertical-align: middle;
                    width: 25px;
                }
            }
        }
    }
}

img {
    max-width: 100%;
    max-height: 100%;
}
</style>