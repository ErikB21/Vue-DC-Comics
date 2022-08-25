<template>
    <header class="container-fluid px-5">
        <nav class="d-flex justify-content-evenly align-items-center ">
            <div class="my_height pe-5 py-1">
                <img src="../assets/img/dc-logo.png" alt="#">
            </div>
            <div class="ps-5">
                <ul class="d-none d-lg-flex justify-content-center align-items-center" >
                    <li v-for="(link, index) in links" :key="index.links" :class=" link.active ? 'active' : '' " class="px-2 list-unstyled"><a class="text-dark py-5 fs-6 text-decoration-none" :href="link.url">{{link.text}}</a></li>
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
   .active a{
        color: $my_color_header !important;
        border-bottom: 4px solid $my_color_header;

   }
   li:hover a{
        border-bottom: 4px solid $my_color_header;
        color: $my_color_header !important; 
    }
    
</style>