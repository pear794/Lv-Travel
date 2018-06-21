<template>
    <div class="banner">
        <div class="home-swiper">
            <swiper :options="swiperOption">
                <!-- slides -->
                <swiper-slide v-for="item in swiperList" :key="item.id">
                    <img class="swiper-img" :src="item.imgUrl" />
                </swiper-slide>
                <!-- Optional controls -->
                <div class="swiper-pagination"  slot="pagination"></div>
            </swiper>
        </div>
        <div class="bannerRadius"></div>
    </div>
</template>

<script>
    export default {
        name : 'HomeSwiper',
        data (){
            return {
                swiperOption : {
                    pagination : '.swiper-pagination',
                    loop : true,
                    autoplay : 2000,
                    speed:500,
                },
                swiperList : [
                    {
                        id : '001',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2018/05/1526627313_76765.jpg'
                    },{
                        id : '002',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2018/05/1526453792_81693.jpg'
                    },{
                        id : '003',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2018/05/1526444428_66273.jpg'
                    },{
                        id : '004',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2018/05/1526455316_99529.jpg'
                    },{
                        id : '005',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2018/06/1528451675_22691.jpg'
                    },{
                        id : '006',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2018/06/1529042205_53990.jpg'
                    }
                ]
            }
        }
    }
</script>

<style lang="stylus" scoped>

    .home-swiper >>> .swiper-pagination-bullet{
        width:5px;
        height:5px;
        background : #fff;
        opacity : 1;
    }
    .home-swiper >>> .swiper-pagination-bullet-active{
        width:20px;
        height:5px;
        background #fff;
        border-radius : 3px;
        z-index : 1;
    }
    .banner{
        position:relative;
        overflow : hidden;
    }
    .home-swiper{
        width : 100%;
        height: 0;
        overflow : hidden;
        padding-bottom:42.66%;
        background #eee;
        position : relative;
        z-index:2;
        .swiper-img{
            width : 100%;
        }
    }
    .bannerRadius{
        width:100%;
        height:6px;
        position : absolute;
        bottom:0;
        left:0;
        background: #fff;
        border-radius: 8px 8px 0 0;
        z-index: 3;
        transform: translateZ(0);
        -webkit-transform: translateZ(0);
    }
    
</style>
