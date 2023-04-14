<script>
import data from "../assets/json/dc-comics.json";
/**
 *proprieta delle immagini
 * thumb link
 * price    
 * series   titolo
 * type     casa editrice
 *   */
export default {
    name: "AppContent",
    computed: {
        imgKey() {
            return Object.values(data);
        },

    }
}
</script>

<template>
    <section class="content">
        <div class="container">
            <div class="card" v-for="(key, index) in imgKey" :key="index">
                {{ key.type }}
            </div>

        </div>

    </section>
</template>

<style scoped lang="scss">
.content {
    background-color: rgb(0, 0, 0);
    color: white;
    padding: 2rem 0;

    .card {
        display: inline-block;
        border: 1px solid white;
        width: 100px;
        height: 100px;
        color: white;
    }
}
</style>