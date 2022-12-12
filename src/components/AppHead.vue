<script >
export default {

}
</script>

<template>

    <header>
        <div class="container">
            <div class="logo">
                <img src="../../public/img/dc-logo.png" alt="">
            </div>
            <nav>
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
            </nav>
        </div>
    </header>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variable' as *;

header {
    height: 120px;
    @include center ();

    .container {
        @include center (space);
        width: 66%;
        height: 100%;

        .logo {

            @include center ();
            height: 100%;

            img {
                width: 80px;
            }
        }

        nav {

            width: 58%;
            height: 100%;

            ul {
                list-style: none;
                @include center ();
                width: 100%;
                height: 100%;

                li {
                    width: calc(100% / 10);
                    height: 100%;
                    @include center ();


                    a {
                        text-decoration: none;
                    }

                    &:active,
                    &:hover {
                        border-bottom: $primary 4px solid;

                        a {
                            color: $primary;

                        }

                    }


                }



            }

        }


    }
}
</style>
