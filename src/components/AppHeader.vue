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
    <section class="header">
        <div class="logo">
            <a href="#">
                <img src="../assets/img/dc-logo.png" alt="">
            </a>
        </div>
        <div class="link">
            <ul>
                <li v-for="link in links" :class="{ active: link.active }"><a :href="link.url">{{ link.name }}</a></li>
            </ul>

        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

.header {
    height: $header_height;
    display: flex;
    min-width: 900px;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 6rem;

    .link {
        a {
            display: block;
            height: 140px;
            text-decoration: none;
            color: inherit;
            text-transform: uppercase;
        }

        li {
            display: inline-block;
            margin-right: 1rem;
            height: $header_height;
            line-height: $header_height;

            &.active,
            &:hover {
                color: $primary_blue;
                border-bottom: 6px solid $primary_blue;
            }
        }
    }
}
</style>