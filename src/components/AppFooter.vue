<script >
export default {
    data() {
        return {
            sections: [
                {
                    title: "DC COMICS",
                    elements: [
                        {
                            title: "Chracters",
                            link: "#"
                        },
                        {
                            title: "Comics",
                            link: "#"
                        },
                        {
                            title: "Movies",
                            link: "#"
                        },
                        {
                            title: "TV",
                            link: "#"
                        },
                        {
                            title: "Games",
                            link: "#"
                        },
                        {
                            title: "Videos",
                            link: "#"
                        },
                        {
                            title: "News",
                            link: "#"
                        },
                    ]
                },
                {
                    title: "SHOP",
                    elements: [
                        {
                            title: "Shop DC",
                            link: "#"
                        },
                        {
                            title: "Shop DC Collectibles",
                            link: "#"
                        },

                    ]
                },

            ],
            dc:
            {
                title: "DC",
                elements: [
                    {
                        title: "Terms Of Use",
                        link: "#"
                    },
                    {
                        title: "Privacy policy (new)",
                        link: "#"
                    },
                    {
                        title: "Ad Choices",
                        link: "#"
                    },
                    {
                        title: "Advertising",
                        link: "#"
                    },
                    {
                        title: "Jobs",
                        link: "#"
                    },
                    {
                        title: "Subscriptions",
                        link: "#"
                    },
                    {
                        title: "Talent Workshops",
                        link: "#"
                    },
                    {
                        title: "CPSC Certificates",
                        link: "#"
                    },
                    {
                        title: "Ratings",
                        link: "#"
                    },
                    {
                        title: "Shop Help",
                        link: "#"
                    },
                    {
                        title: "Contact Us",
                        link: "#"
                    },
                ]
            },

            sites:
            {
                title: "SITES",
                elements: [
                    {
                        title: "DC",
                        link: "#"
                    },
                    {
                        title: "MAD Magazine",
                        link: "#"
                    },
                    {
                        title: "DC Kids",
                        link: "#"
                    },
                    {
                        title: "DC Universe",
                        link: "#"
                    },
                    {
                        title: "DC Power Visa",
                        link: "#"
                    },

                ]
            },

            footerImgs: [
                {
                    img: this.getImageUrl('../../public/img/footer-facebook.png'),
                },
                {
                    img: this.getImageUrl('../../public/img/footer-periscope.png'),
                },
                {
                    img: this.getImageUrl('../../public/img/footer-pinterest.png'),
                },
                {
                    img: this.getImageUrl('../../public/img/footer-twitter.png'),
                },
                {
                    img: this.getImageUrl('../../public/img/footer-youtube.png'),
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


    <footer>
        <div class="container">
            <div class="sizing">
                <div class="box">
                    <ul v-for="section, index in sections" :key="index">
                        <h3>{{ section.title }}</h3>
                        <li v-for="(element, index) in section.elements" :key="index">
                            <a href="element.link">{{ element.title }}</a>
                        </li>
                    </ul>
                </div>
                <div class="box">
                    <ul>
                        <h3>{{ dc.title }}</h3>
                        <li v-for="(element, index) in dc.elements" :key="index">
                            <a href="element.link">{{ element.title }}</a>
                        </li>
                    </ul>
                </div>
                <div class="box">
                    <ul>
                        <h3>{{ sites.title }}</h3>
                        <li v-for="(element, index) in sites.elements" :key="index">
                            <a href="element.link">{{ element.title }}</a>
                        </li>
                    </ul>
                </div>
                <div class="logo-big">
                    <img :src="getImageUrl('../../public/img/dc-logo-bg.png')" alt="">
                </div>
            </div>
        </div>
        <div class="bottom-container">
            <div class="bottom">
                <div class="button">
                    <h3>SING - UP NOW</h3>
                </div>
                <div class="social">
                    <h3>FOLLOW US</h3>
                    <img v-for="image, index in footerImgs" :key="index" :src="image.img" alt="">
                </div>
            </div>

        </div>

    </footer>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variable' as *;


.container {
    background-image: url("../../public/img/footer-bg.jpg");
    overflow: hidden;
    background-size: cover;
    height: 450px;
    filter: grayscale(100);
    @include center ();

    .sizing {
        width: $mainSize;
        display: flex;

        div {
            margin-right: 50px;

            ul {

                margin-top: 70px;
                list-style: none;
                width: 103%;


                h3 {
                    color: $secondary;
                    margin: 20px 0;
                }


                li {
                    padding: 3px 0;
                    font-size: 0.8rem;

                    a {
                        color: $trd;
                        text-decoration: none;
                    }

                }



            }
        }

        img {
            margin-left: 350px;

        }
    }



}

.bottom-container {

    background-color: $frth;
    @include center ();

    .bottom {
        width: calc($mainSize);
        height: 100px;
        @include center (horizontal);
        justify-content: space-between;

        .button {
            height: 60px;
            border: $primary solid 2px;
            width: 180px;
            color: $secondary;
            @include center ();
        }


    }

    .social {
        color: $primary;
        @include center ();

        img {
            margin-left: 15px;
        }
    }
}
</style>
