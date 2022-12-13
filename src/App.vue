<script>
import AppHead from './components/AppHead.vue'
import AppCards from './components/AppCards.vue'
import AppFooter from './components/AppFooter.vue'
import Body from './components/Body.vue'


export default {
  components: {
    AppHead,
    AppCards,
    AppFooter,
    Body
  },
}
</script>

<template>
  <AppHead />
  <main>

    <Body />
  </main>
  <AppCards />
  <AppFooter />
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/mixins' as *;
@use './styles/partials/variable' as *;
</style>
