<template>
    <div class="card border border-0 pt-5">
        <img :src="imageSrc" :alt="title">
        <h3 class="h5 text-white text-center py-1">{{title}}</h3>
    </div>
</template>

<script>
export default {
    name: 'CardComics',
    props: {
        imageSrc: String,
        title: String
    }
}
</script>

<style scoped lang="scss">
    @import '../assets/style/vars.scss';
    .card{
      width: calc(100% / 6 - 100px);
      height: calc(100% / 2);
      margin: 10px 50px;
      background-color: $bg_main;
      img{
        width: 100%;
      }
    }
</style>