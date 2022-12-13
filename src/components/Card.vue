<script >
export default {


};
</script>

<template>

    <li>
        <div>
            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                alt="">
        </div>

        <h5>ACTION COMICS</h5>
    </li>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variable' as *;

div {
    height: 100px;
    width: 100px;
    overflow: hidden;

}

h5 {
    color: $secondary;
    font-size: 0.5rem;
    margin: 10px 0;
}
</style>
