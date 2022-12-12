<script>
import AppHead from './components/AppHead.vue'


export default {
  components: {
    AppHead
  },
}
</script>

<template>
  <AppHead />
  <main>
    <h1>CONTENT GOES HERE</h1>
  </main>
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/mixins' as *;
@use './styles/partials/variable' as *;

main {
  color: $secondary;
  width: $mainSize;
  height: 200px;
  @include center ();

}
</style>
