<script >
import Jumbo from './Jumbo.vue'
import JumboButton from './JumboButton.vue'

export default {
    components: {
        Jumbo,
        JumboButton
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
        <JumboButton class="button" />
    </div>


</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variable' as *;


.body-container {
    width: $mainSize;
    @include center (space);

    .button {
        position: absolute;
        top: 500px;
        left: 300px;
    }
}
</style>
