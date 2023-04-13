<script>
export default {
    name: "AppContent",
}
</script>

<template>
    <section class="call-to-action">
        <div class="container">
            sono call to action
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
}
</style>