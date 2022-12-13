<script >
import Jumbo from './Jumbo.vue'
import JumboButton from './JumboButton.vue'
import Card from './Card.vue'
import json from '../../dc-comics.json'


export default {
    components: {
        Jumbo,
        JumboButton,
        Card
    },
    data() {
        return {
            myJson: json,
            textButtons: ["CURRENT SERIES", "LOAD MORE"]

        };

    },
    methods: {
        getImageUrl: function (imgPath) {
            return new URL('../../public/img/${imgPath}');

        }
    }

};
</script>

<template>

    <Jumbo />
    <div class="body-container">
        <div class="wrapper">
            <JumboButton class="button" :text="textButtons[0]" />
            <ul>
                <Card v-for="(element, index) in myJson" :key="index" :thumb="element.thumb" :series="element.series" />
            </ul>
            <div class="button-container">
                <JumboButton class="second" :text="textButtons[1]" />
            </div>

        </div>

    </div>


</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variable' as *;


.body-container {
    @include center ();

    .wrapper {
        width: $mainSize;

        .button {
            position: absolute;
            top: 500px;
            left: 300px;
        }

        ul {
            margin: 40px 0;
            @include center ();
            flex-wrap: wrap;
        }

        .second {
            position: relative;
            top: 0;
            left: 0;
        }

        .button-container {
            @include center ();
            margin-bottom: 20px;
        }
    }
}
</style>
