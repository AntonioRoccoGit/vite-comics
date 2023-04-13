<script>

export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    name: "characters",
                    url: "#",
                    active: false
                },
                {
                    name: "comics",
                    url: "#",
                    active: true
                },
                {
                    name: "movies",
                    url: "#",
                    active: false
                },
                {
                    name: "tv",
                    url: "#",
                    active: false
                },
                {
                    name: "games",
                    url: "#",
                    active: false
                },
                {
                    name: "collectibles",
                    url: "#",
                    active: false
                },
                {
                    name: "videos",
                    url: "#",
                    active: false
                },
                {
                    name: "fans",
                    url: "#",
                    active: false
                },
                {
                    name: "news",
                    url: "#",
                    active: false
                },
                {
                    name: "shop",
                    url: "#",
                    active: false
                }
            ],
        }
    }

}
</script>

<template>
    <div class="container">
        <section class="header">
            <div class="logo">
                <a href="#">
                    <img src="../assets/img/dc-logo.png" alt="">
                </a>
            </div>
            <div class="link">
                <svg class="hamburg" xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 448 512"><!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                    <path
                        d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z" />
                </svg>
                <ul>
                    <li v-for="link in links" :class="{ active: link.active }"><a :href="link.url">{{ link.name }}</a></li>
                </ul>

            </div>
        </section>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

.header {
    height: $header_height;
    display: flex;
    align-items: center;
    justify-content: space-between;

    .hamburg {
        display: none;
        color: $primary_blue;
        cursor: pointer;
    }

    .logo img {
        height: 60px;
    }

    .link {

        a {
            display: block;
            height: $header_height;
            text-decoration: none;
            color: inherit;
            text-transform: uppercase;
        }

        li {
            text-align: center;
            display: inline-block;
            min-width: 30px;
            margin-right: 1rem;
            height: $header_height;
            line-height: $header_height;
            font-size: .6rem;
            font-weight: 900;

            &.active,
            &:hover {
                color: $primary_blue;
                border-bottom: 6px solid $primary_blue;
            }
        }
    }

}

@media screen and (max-width: 900px) {
    .link ul {
        display: none;
    }

    .header .hamburg {
        display: block;
        width: 40px;
    }
}
</style>