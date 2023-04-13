<script >
// components
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppCallToAction from './components/AppCallToAction.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppContent,
    AppCallToAction,
    AppFooter
  }
}
</script>

<template>
  <AppHeader />
  <AppContent />
  <AppCallToAction />
  <AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss" as *;
</style>
