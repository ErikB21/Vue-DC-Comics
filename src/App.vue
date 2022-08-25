<template>
  <div id="app">
    <HeaderComics/>
    <MainComics/>
    <SectionMain/>
    <FooterComics/>
  </div>
</template>

<script>
import MainComics from './components/MainComics.vue';
import HeaderComics from './components/HeaderComics.vue';
import FooterComics from './components/FooterComics.vue';
import SectionMain from './components/SectionMain.vue';
export default {
  name: 'App',
  components: {
    MainComics,
    HeaderComics,
    FooterComics,
    SectionMain
}
}
</script>


<style lang="scss">
  @import './assets/style/utilities.scss';
  @import './assets/style/vars.scss';
</style>
