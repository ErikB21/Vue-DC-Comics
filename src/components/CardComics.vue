<template>
    <div class="card border border-0 px-0 pt-5">
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
        max-width: calc(100% / 6 - 30px);
        max-height: calc(100% / 2);
        margin: 10px 15px;
        background-color: $bg_main;
        
        img{
            width: 100%;
            &:hover{
            box-shadow: 10px 5px 5px 5px black;
            opacity: 0.6;
            transform: perspective(12cm) rotateX(-15deg) rotateY(30deg);
            }   
        }
    }
</style>