<template>
  <div id="app">
    <HeaderComics/>
    <MainComics/>
    <FooterComics/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import MainComics from './components/MainComics.vue';
import HeaderComics from './components/HeaderComics.vue';
import FooterComics from './components/FooterComics.vue';

export default {
  name: 'App',
  components: {
    MainComics,
    HeaderComics,
    FooterComics
}
}
</script>

<style lang="scss">

</style>
