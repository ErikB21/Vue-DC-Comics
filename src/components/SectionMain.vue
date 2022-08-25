<template>
    <div class="container-fluid">
        <div class="row bg-primary py-2">
           <div class="col-12 col-md-8 justify-content-center m-auto">
                <ul  class="list-unstyled my_role d-flex flex-wrap py-3 justify-content-evenly align-items-center">
                    <li v-for="(link,index) in linksLogo" :key="index.linksLogo" class="rounded-5 py-4 px-2 d-flex justify-content-center align-items-center list-unstyled">
                        <a class="text-white text-decoration-none d-flex justify-content-evenly align-items-center" href="#">
                            <img :src="link.url" :alt="link.title"/>
                            <span class="px-1">{{link.title}}</span>
                        </a>
                    </li>
                </ul>
           </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SectionMain',
    data(){
        return{
            linksLogo:[
                {
                    url: require('@/assets/img/buy-comics-digital-comics.png'),
                    title:'DIGITAL COMICS'

                },
                {
                    url: require('@/assets/img/buy-comics-merchandise.png'),
                    title:'DC MERCHANDISE'

                },
                {
                    url: require('@/assets/img/buy-comics-subscriptions.png'),
                    title:'SUBSCRIPTION'

                },
                {
                    url: require('@/assets/img/buy-comics-shop-locator.png'),
                    title:'COMIC SHOP LOCATOR'

                },
                {
                    url: require('@/assets/img/buy-dc-power-visa.svg'),
                    title:'DC POWER VISA'

                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../assets/style/vars.scss';
    .my_role {
        li:hover{
            background-color: $my_color_header;
            opacity: 0.6;
        }
        img{
            height: 50px; 
        }
    }
</style>