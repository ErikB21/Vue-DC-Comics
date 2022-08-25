<template>
    <footer class="container-fluid ">

        <div class="row my_personal_bg justify-content-center">
            <div class="col-12 col-md-6 col-lg-5 d-flex justify-content-center pt-3">

                <div class="px-3">
                    <h3 class="text-white">DC COMICS</h3>
                    <ul class="p-0">
                        <li v-for="(link,index) in links" :key="index.links" class="fs-6 list-unstyled"><a class="text-decoration-none fs-6" href="">{{link.link}}</a></li>
                    </ul>
                    <h3 class="text-white">SHOP</h3>
                    <ul class="p-0">
                        <li class="fs-6 list-unstyled"><a class="text-decoration-none fs-6" href="">Shop DC</a></li>
                        <li class="fs-6 list-unstyled"><a class="text-decoration-none fs-6" href="">Shop DC Collectibles</a></li>
                    </ul>        
                </div>

                <div class="px-3">
                    <h3 class="text-white">DC</h3>
                    <ul class="p-0">
                        <li v-for="(link,index) in linksTwo" :key="index.linksTwo" class="fs-6 list-unstyled"><a class="text-decoration-none fs-6" href="">{{link.link}}</a></li>
                    </ul>
                </div>

                <div class="px-3">
                    <h3 class="text-white">SITES</h3>
                    <ul class="p-0">
                        <li v-for="(link,index) in linksThree" :key="index.linksThree" class="fs-6 list-unstyled"><a class="text-decoration-none fs-6" href="">{{link.link}}</a></li>
                    </ul>
                </div>
            </div>         
            <div class="d-none d-lg-block col-lg-6 my_personal_bg_logo"></div>
        </div>
        <div class="row my_personal_color_bg py-3">
            <div class="col-12 d-flex justify-content-around align-items-center m-auto">
                <div class="btn border-primary rounded-0 p-3 text-white">
                    SIGN-UP NOW!
                </div>
                <div class="section_social">
                    <span class="px-2 text-primary">FOLLOW US</span>
                    <a v-for="(link,index) in logoLinks" :key="index.logoLinks" :href="link.url"><img  class="px-1" :src="link.link" alt=""/></a>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'FooterComics',
    data(){
        return{
            links:[
                {
                    link: 'Characters'
                },
                {
                    link: 'Comics'
                },
                {
                    link: 'Movies'
                },
                {
                    link: 'TV'
                },
                {
                    link: 'Games'
                },
                {
                    link: 'Videos'
                },
                {
                    link: 'News'
                }
            ],
            linksTwo:[
                {
                    link: 'Terms Of Use'
                },
                {
                    link: 'Privacy Police'
                },
                {
                    link: 'Ad Choices'
                },
                {
                    link: 'Advertising'
                },
                {
                    link: 'Jobs'
                },
                {
                    link: 'Subscriptions'
                },
                {
                    link: 'Talent Workshop'
                },
                {
                    link: 'CPSC Certificates'
                },
                {
                    link: 'Ratings'
                },
                {
                    link: 'Shop Help'
                },
                {
                    link: 'Contact Us'
                }
            ],
            linksThree:[
                {
                    link: 'DC'
                },
                {
                    link: 'MAD Magazine'
                },
                {
                    link: 'DC Kids'
                },
                {
                    link: 'DC Universe'
                },
                {
                    link: 'DC Power Visa'
                }
            ],
            logoLinks:[
                {
                    link: require('@/assets/img/footer-facebook.png'),
                    url: 'https://www.facebook.com/dc/'
                },
                {
                    link: require('@/assets/img/footer-twitter.png'),
                    url: 'https://twitter.com/dccomics'
                },
                {
                    link: require('@/assets/img/footer-youtube.png'),
                    url: 'https://www.youtube.com/channel/UCiifkYAs_bq1pt_zbNAzYGg'
                },
                {
                    link: require('@/assets/img/footer-pinterest.png'),
                    url: 'https://www.pinterest.it/dccomics/'
                },
                {
                    link: require('@/assets/img/footer-periscope.png'),
                    url: 'https://www.chsperiscope.com/tag/dc-comics/'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../assets/style/vars.scss';
    
    
    .my_personal_bg{
        background-image:url(../assets/img/footer-bg.jpg);
        background-size:cover;
        padding: 0 180px;
        a{
            color:$color_links;
        }
        .my_personal_bg_logo{
            background-image: url(../assets/img/dc-logo-bg.png);
            background-size: 400px;
            background-repeat: no-repeat;
            background-position-x: center;
            background-position-y: center;
        }   
    }
    .my_personal_color_bg{
        background-color: $bg_color_footer;
        .btn:hover{
            background-color: $button_hover_bg;
            color: $color_black !important;
        }
    }
</style>