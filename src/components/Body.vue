<script >
import Jumbo from './Jumbo.vue'
import JumboButton from './JumboButton.vue'
import Card from './Card.vue'


export default {
    components: {
        Jumbo,
        JumboButton,
        Card
    },
    data() {
        return {


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
            <JumboButton class="button" />
            <ul>
                <Card />
            </ul>
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
            margin-top: 40px;
        }
    }
}
</style>
