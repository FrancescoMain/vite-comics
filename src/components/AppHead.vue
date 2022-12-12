<script >
export default {
    data() {
        return {
            links: [
                {
                    title: 'CHARACTERS',
                    link: '#'
                },
                {
                    title: 'COMICS',
                    link: '#'
                },
                {
                    title: 'MOVIES',
                    link: '#'
                },
                {
                    title: 'TV',
                    link: '#'
                },
                {
                    title: 'GAMES',
                    link: '#'
                },
                {
                    title: 'COLLECTIBLES',
                    link: '#'
                },
                {
                    title: 'VIDEOS',
                    link: '#'
                },
                {
                    title: 'FANS',
                    link: '#'
                },
                {
                    title: 'NEWS',
                    link: '#'
                },
                {
                    title: 'SHOP',
                    link: '#'
                },
            ]

        };

    },
    methods: {
        getImageUrl: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }

};
</script>

<template>

    <header>
        <div class="container">
            <div class="logo">
                <img :src="getImageUrl('../../public/img/dc-logo.png')" alt="">
            </div>
            <nav>
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a href="link.link">{{ link.title }}</a>
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
    background-color: $secondary;
    height: 120px;
    @include center ();

    .container {
        @include center (space);
        width: $mainSize;
        height: 100%;

        .logo {
            @include center ();
            height: 100%;

            img {
                width: 80px;
            }
        }

        nav {
            width: 70%;
            height: 100%;

            ul {
                list-style: none;
                @include center ();
                width: 100%;
                height: 100%;

                li {
                    padding: 0 20px;
                    height: 100%;
                    font-size: 0.7rem;
                    font-weight: 600;
                    @include center ();


                    a {
                        text-decoration: none;
                    }

                    &:active,
                    &:hover {
                        border-bottom: $primary 4px solid;
                        cursor: pointer;

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
