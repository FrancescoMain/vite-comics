<script >
export default {

}
</script>

<template>
    <div class="container">
        <div class="logo">
            <img src="../../public/img/dc-logo.png" alt="">
        </div>
        <ul>
            <li>
                <a href="">Link</a>
            </li>
            <li>
                <a href="">Link</a>
            </li>
            <li>
                <a href="">Link</a>
            </li>
            <li>
                <a href="">Link</a>
            </li>
            <li>
                <a href="">Link</a>
            </li>
            <li>
                <a href="">Link</a>
            </li>
            <li>
                <a href="">Link</a>
            </li>
            <li>
                <a href="">Link</a>
            </li>
            <li>
                <a href="">Link</a>
            </li>
            <li>
                <a href="">Link</a>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/mixins' as *;

.container {
    @include center (space);
    height: 100px;
    background-color: aqua;

    ul {
        list-style: none;
        @include center ();

        li {

            a {
                text-decoration: none;
            }
        }

    }
}
</style>
