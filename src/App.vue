<script>
import AppHead from './components/AppHead.vue'
import AppCards from './components/AppCards.vue'


export default {
  components: {
    AppHead,
    AppCards
  },
}
</script>

<template>
  <AppHead />
  <main>
    <h1>CONTENT GOES HERE</h1>
  </main>
  <AppCards />
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/mixins' as *;
@use './styles/partials/variable' as *;

main {
  color: $secondary;
  width: $mainSize;
  height: 150px;
  @include center ();

}
</style>
