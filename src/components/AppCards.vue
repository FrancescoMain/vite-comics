<script >
export default {
    data() {
        return {
            links: [
                {
                    title: 'DIGITAL COMICS',
                    link: '#',
                    img: this.getImageUrl("../../public/img/buy-comics-digital-comics.png")
                },
                {
                    title: 'DC MERCHANDISE',
                    link: '#',
                    img: this.getImageUrl("../../public/img/buy-comics-merchandise.png")

                },
                {
                    title: 'SUBSCRIPTION',
                    link: '#',
                    img: this.getImageUrl("../../public/img/buy-comics-subscriptions.png")
                },
                {
                    title: 'COMIC SHOP LOCATION',
                    link: '#',
                    img: this.getImageUrl("../../public/img/buy-comics-shop-locator.png")
                },
                {
                    title: 'DC POWER VISA',
                    link: '#',
                    img: this.getImageUrl("../../public/img/buy-dc-power-visa.svg")
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

    <div class="container">
        <ul>
            <li v-for="(link, index) in links" :key="index">
                <img :src="link.img" alt="">
                <a href="link.link">{{ link.title }}</a>
            </li>
        </ul>
    </div>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variable' as *;

.container {
    background-color: $primary;
    height: 120px;
    @include center ();

    ul {

        list-style: none;
        @include center ();
        width: 100%;
        height: 100%;

        li {
            padding: 0 20px;
            height: 100%;
            @include center ();

            img {
                width: 40px;
            }


            a {
                color: $secondary;
                text-decoration: none;
                margin: 0 10px;
            }





        }



    }

}
</style>
