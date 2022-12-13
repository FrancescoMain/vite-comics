<script >
import Jumbo from './Jumbo.vue'

export default {
    components: {
        Jumbo
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

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variable' as *;
</style>
