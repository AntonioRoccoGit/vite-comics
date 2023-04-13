<script>
export default {
    name: "AppContent",
    data() {
        return {
            shopLinks: [
                {
                    img: "buy-comics-digital-comics.png",
                    title: "digital comics",
                    url: "#",
                    custom: false
                },
                {
                    img: "buy-comics-merchandise.png",
                    title: "dc merchandise",
                    url: "#",
                    custom: false
                },
                {
                    img: "buy-comics-subscriptions.png",
                    title: "subscription",
                    url: "#",
                    custom: false
                },
                {
                    img: "buy-comics-shop-locator.png",
                    title: "comic shop locator",
                    url: "#",
                    custom: false
                },
                {
                    img: "buy-dc-power-visa.svg",
                    title: "dc power visa",
                    url: "#",
                    custom: false
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
    <section class="call-to-action">
        <div class="container">
            <ul>
                <li v-for="item in shopLinks">
                    <a :href="item.url">
                        <img :class="{ custom: item.custom }" :src="getImgPath(item)" alt="">
                        <h2>{{ item.title }}</h2>
                    </a>
                </li>

            </ul>

        </div>

    </section>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

.call-to-action {
    padding: 2rem 0;
    position: relative;
    background-color: $primary_blue;
    z-index: 10;

    ul {
        list-style-type: none;
        display: flex;
        justify-content: space-around;

        a {
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;

            h2 {
                font-size: .7rem;
                font-weight: 400;
                text-transform: uppercase;
                margin-left: .6rem;
            }
        }

        img {
            width: 40px;
            height: 40px;
            object-fit: contain;
            // &.custom {
            //     object-fit: contain;
            // }
        }
    }
}
</style>