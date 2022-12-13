<script >
export default {
    methods: {
        getImageUrl: function (imgPath) {
            return new URL(`../../public/img/${imgPath}`, import.meta.url).href;
        }
    }

};
</script>

<template>
    <div class="jumbo"></div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variable' as *;

.jumbo {
    background-image: url("../../public/img/jumbotron.jpg");
    height: 400px;
    width: 100%;
}
</style>
