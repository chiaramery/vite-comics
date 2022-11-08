<script>
import AppHeader from './components/AppHeader.vue';
import ContentHere from './components/ContentHere.vue';
import AppFooter from './components/AppFooter.vue';

export default {
    components: {
        AppHeader,
        ContentHere,
        AppFooter,
    }
}
</script>

<template>

    <AppHeader />
    <ContentHere />
    <AppFooter />

</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>