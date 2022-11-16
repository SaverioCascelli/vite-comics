<script>
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import AppMain from './components/AppMain.vue';
import AppCallToAction from './components/AppCallToAction.vue';
import AppJumbotron from './components/AppJumbotron.vue';

export default {
  name: 'App',
  components: {
    AppFooter,
    AppHeader,
    AppCallToAction,
    AppMain,
    AppJumbotron
  }
}
</script>


<template>
  <AppHeader />
  <AppJumbotron />
  <AppMain />
  <AppCallToAction/>
  <AppFooter />
</template>


<style lang="scss">
@use './styles/general.scss';
</style>
