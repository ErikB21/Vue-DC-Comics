<template>
    <header class="container-fluid px-5">
        <nav class="d-flex justify-content-evenly align-items-center py-2">
            <div class="my_height pe-5">
                <img src="../assets/img/dc-logo.png" alt="#">
            </div>
            <div class="ps-5">
                <ul class="d-none d-lg-flex justify-content-center align-items-center" >
                    <li v-for="(link, index) in links" :key="index.links" :class=" link.active ? 'active' : '' " class="px-2 list-unstyled"><a class="text-dark fs-6 text-decoration-none" :href="link.url">{{link.text}}</a></li>
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
   .active a{
        color: royalblue !important;
        border-bottom: 2px solid royalblue;

   }
   li:hover a{
        border-bottom: 2px solid royalblue;
        color: royalblue !important; 
    }
</style>