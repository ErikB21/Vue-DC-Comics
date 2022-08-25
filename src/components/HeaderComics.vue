<template>
    <header class="container-fluid px-5">
        <nav class="d-flex justify-content-evenly align-items-center ">
            <div class="my_height pe-5 py-1">
                <img src="../assets/img/dc-logo.png" alt="#">
            </div>
            <div class="ps-5">
                <ul class="d-none d-lg-flex justify-content-center align-items-center" >
                    <li v-for="(link, index) in links" :key="index.links" :class=" link.active ? 'active' : '' " class="cl-effect-12 position-relative px-3 list-unstyled"><a class="text-dark py-5 fs-6 text-decoration-none" :href="link.url">{{link.text}}</a></li>
                </ul>
            </div>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'HeaderComics',
    data(){
        return{
            links:[
                {
                    text: 'CHARACTERS',
                    url: '#',
                    active: false
                },
                {
                    text: 'COMICS',
                    url: '#',
                    active: true
                },
                {
                    text: 'MOVIES',
                    url: '#',
                    active: false
                },
                {
                    text: 'TV',
                    url: '#',
                    active: false
                },
                {
                    text: 'GAMES',
                    url: '#',
                    active: false
                },
                {
                    text: 'COLLECTIBLES',
                    url: '#',
                    active: false
                },
                {
                    text: 'VIDEOS',
                    url: '#',
                    active: false
                },
                {
                    text: 'FANS',
                    url: '#',
                    active: false
                },
                {
                    text: 'NEWS',
                    url: '#',
                    active: false
                },
                {
                    text: 'SHOP',
                    url: '#',
                    active: false
                }
            ]
        }   
    }
}
</script>

<style scoped lang="scss">
    @import '../assets/style/vars.scss';
    .cl-effect-12 a::before,
    .cl-effect-12 a::after {
        position: absolute;
        top: 50%;
        left: 50%;
        width: 80px;
        height: 80px;
        border: 2px solid rgba(0,0,0,0.1);
        border-radius: 50%;
        content: '';
        opacity: 0;
        -webkit-transition: -webkit-transform 0.3s, opacity 0.3s;
        -moz-transition: -moz-transform 0.3s, opacity 0.3s;
        transition: transform 0.3s, opacity 0.3s;
        -webkit-transform: translateX(-50%) translateY(-50%) scale(0.2);
        -moz-transform: translateX(-50%) translateY(-50%) scale(0.2);
        transform: translateX(-50%) translateY(-50%) scale(0.2);
    }

    .cl-effect-12 a::after {
        width: 70px;
        height: 70px;
        border-width: 6px;
        -webkit-transform: translateX(-50%) translateY(-50%) scale(0.8);
        -moz-transform: translateX(-50%) translateY(-50%) scale(0.8);
        transform: translateX(-50%) translateY(-50%) scale(0.8);
    }

    .cl-effect-12 a:hover::before,
    .cl-effect-12 a:hover::after,
    .cl-effect-12 a:focus::before,
    .cl-effect-12 a:focus::after {
        opacity: 1;
        -webkit-transform: translateX(-50%) translateY(-50%) scale(1);
        -moz-transform: translateX(-50%) translateY(-50%) scale(1);
        transform: translateX(-50%) translateY(-50%) scale(1);
    }
    
</style>