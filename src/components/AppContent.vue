<script>
import data from "../assets/json/dc-comics.json";
import ContentCard from "./ContentCard.vue";
/**
 *proprieta delle immagini
 * thumb    link
 * price    
 * series   titolo
 * type     genere
 *   */
export default {
    name: "AppContent",
    components: {
        ContentCard
    },
    computed: {
        imgKey() {
            return Object.values(data);
        },
    }
}
</script>

<!-- <div class="card" v-for="(key, index) in imgKey" :key="index">
    {{ key.type }}
</div> -->

<template>
    <div class="jumbotron">
        <img src="../assets/img/jumbotron.jpg" alt="">
    </div>
    <div class="content">

        <div class="container">
            <h2 class="label">
                CURRENT SERIES
            </h2>
            <div class="row">
                <ContentCard v-for="(key, index) in imgKey" :key="index" :title="key.series" :url="key.thumb"
                    :alt="key.type" />

            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

.jumbotron {
    height: 180px;

    img {
        height: 600px;
        width: 100%;
        display: block;
        object-fit: cover;
    }
}

.content {
    position: relative;
    background-color: $content_bg_color;
    color: white;
    z-index: 999;

    .label {
        background-color: $primary_blue;
        position: absolute;
        font-size: .8rem;
        padding: .5rem 1rem;
        top: -15px;
        left: 100px;
    }

    .container {
        padding-top: .4rem;

        .row {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }
    }
}
</style>