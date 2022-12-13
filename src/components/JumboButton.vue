<script >
export default {
    props: {
        text: String,
    },
    methods: {
        getImageUrl: function (imgPath) {
            return new URL(`../../public/img/${imgPath}`, import.meta.url).href;
        }
    }

};
</script>

<template>

    <button class="button">{{ text }}</button>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variable' as *;



.button {
    width: 180px;
    height: 45px;
    font-size: 0.9rem;
    text-transform: uppercase;
    font-weight: 700;
    color: $secondary;
    background-color: $primary;
    border: none;
    box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease 0s;
    cursor: pointer;
    outline: none;

    &:hover {
        background-color: $secondary;
        box-shadow: 0px 15px 20px $trd;
        color: rgb(0, 0, 0);
        transform: translateY(-7px);
    }
}
</style>
