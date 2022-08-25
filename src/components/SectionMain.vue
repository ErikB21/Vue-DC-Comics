<template>
    <div class="container-fluid">
        <div class="row bg-primary py-2">
           <div class="col-12 col-md-9 justify-content-center m-auto">
                <ul  class="list-unstyled my_role d-flex flex-wrap py-5 justify-content-evenly align-items-center">
                    <li v-for="(link,index) in linksLogo" :key="index.linksLogo" class="cl-effect-18 rounded-5 py-4 px-2 d-flex justify-content-center align-items-center list-unstyled">
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
        
        img{
            height: 50px; 
        }
        .cl-effect-18 {
            position: relative;
            z-index: 1;
        }

        .cl-effect-18 a {
            -webkit-transition: color 0.3s;
            -moz-transition: color 0.3s;
            transition: color 0.3s;
        }

        .cl-effect-18 a::before,
        .cl-effect-18 a::after {
            position: absolute;
            width: 100%;
            left: 0;
            top: 50%;
            height: 4px;
            margin-top: -1px;
            background: $my_color_header;
            content: '';
            z-index: -1;
            -webkit-transition: -webkit-transform 0.3s, opacity 0.3s;
            -moz-transition: -moz-transform 0.3s, opacity 0.3s;
            transition: transform 0.3s, opacity 0.3s;
            pointer-events: none;
        }

        .cl-effect-18 a::before {
            -webkit-transform: translateY(-20px);
            -moz-transform: translateY(-20px);
            transform: translateY(-20px);
        }

        .cl-effect-18 a::after {
            -webkit-transform: translateY(20px);
            -moz-transform: translateY(20px);
            transform: translateY(20px);
        }

        .cl-effect-18 a:hover,
        .cl-effect-18 a:focus {
            color: #fff;
        }

        .cl-effect-18 a:hover::before,
        .cl-effect-18 a:hover::after,
        .cl-effect-18 a:focus::before,
        .cl-effect-18 a:focus::after {
            opacity: 0.7;
        }

        .cl-effect-18 a:hover::before,
        .cl-effect-18 a:focus::before {
            -webkit-transform: rotate(45deg);
            -moz-transform: rotate(45deg);
            transform: rotate(45deg);
        }

        .cl-effect-18 a:hover::after,
        .cl-effect-18 a:focus::after {
            -webkit-transform: rotate(-45deg);
            -moz-transform: rotate(-45deg);
            transform: rotate(-45deg);
        }
    }
</style>