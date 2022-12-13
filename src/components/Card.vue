<script >
export default {
    props: {
        thumb: String,
        series: String,
    }

};
</script>

<template>

    <li>
        <div class="wrapper">
            <div class="img-container">
                <img :src="thumb" alt="">
            </div>

            <h5>{{ series }}</h5>
        </div>

    </li>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variable' as *;

li {
    width: calc(100% / 5 - 42px);
    @include center ();

    .img-container {
        height: 200px;
        width: 200px;
        overflow: hidden;
        margin-bottom: 30px;
    }

    h5 {
        color: $secondary;
        font-size: 0.9rem;
        margin: 10px 0;
    }
}
</style>
