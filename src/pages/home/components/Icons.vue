<template>
    <div class="small-icon">
        <div class="icons">
            <div class="icon" v-for="list in imgList" :key="list.id">
                <div class="icon-img">
                    <img class="icon-imgcontent" :src="list.imgUrl" />
                </div>
                <p class="icon-desc">{{ list.desc }}</p>
            </div>
        </div>
        <div class="headline">
            <span class="title"></span>
            <div class="swiper">
                <swiper :options="swiperOption">
                    <!-- slides -->
                    <swiper-slide>
                        <p>这样边吃边玩长沙、张家界，不用动脑筋！</p>
                    </swiper-slide>
                    <swiper-slide>
                        <p>昆明 | 自然景观和人文景观的荟萃之地</p>
                    </swiper-slide>
                    <swiper-slide>
                        <p>比东京迪士尼还要嗨！日本环球影城终极攻略！</p>
                    </swiper-slide>
                </swiper>
            </div>
            <span class="more"></span>
        </div>
    </div>
</template>

<script>
    export default {
        name : 'HomeIcons',
        data (){
            return {
                swiperOption : {
                    direction: 'vertical',
                    pagination : '.swiper-pagination',
                    loop : true,
                    autoplay : 2000,
                    speed:1000,
                    clickable : true,
                    vertical : true
                },
                imgList : [
                    {
                        id : '001',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2018/01/1516938549_25686.png',
                        desc : '旅行必备'
                    },
                    {
                        id : '002',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2017/12/1514474349_75047.png',
                        desc : '自驾游'
                    },
                    {
                        id : '003',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2018/05/1525256515_44403.png',
                        desc : '国际机票'
                    },
                    {
                        id : '004',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2017/12/1514474245_92479.png',
                        desc : '驴悦亲子游'
                    },
                    {
                        id : '005',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2018/05/1526266490_17194.png',
                        desc : '国内用车'
                    },
                    {
                        id : '006',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2018/05/1526023291_25260.png',
                        desc : '特卖会'
                    },
                    {
                        id : '007',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2018/04/1523252783_60535.png',
                        desc : '签到'
                    },
                    {
                        id : '008',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2017/12/1514474202_85264.png',
                        desc : '签证'
                    },
                    {
                        id : '009',
                        imgUrl : 'https://pics.lvjs.com.cn/pics/super/2018/03/1520416990_47578.png',
                        desc : '万达乐园'
                    },
                    {
                        id : '010',
                        imgUrl : '//pics.lvjs.com.cn/mobile/node_pro/projects/homepage/static/images/moreIcon.png?v=2018',
                        desc : '更多'
                    },
                ]
            }
        }
    }
</script>

<style lang="stylus" scoped>
    .small-icon{
        width : 100%;
        height:0;
        background : #fff;
        overflow : hidden;
        padding-bottom:55%;
        padding-top:10px;
        padding-left:10px;
        padding-right:10px;
        box-sizing:border-box;
        .icons{
            width:100%;
            height:0;
            padding-bottom:42%;
            border-bottom:1px solid #E0E0E0;
            .icon:first-child .icon-img::before{
                content : '商品';
                display : block;
                width : 30px;
                height : 15px;
                line-height : 15px;
                font-size : 12px;
                position : absolute;
                text-align : center;
                top : 0;
                right : 0;
                background : #f60;
                color : #fff;
                border-top-left-radius : 5px;
                border-top-right-radius : 5px;
                border-bottom-right-radius : 5px;

            }
            .icon{
                overflow : hidden;
                float : left;
                width : 20%;
                height:0;
                padding-bottom : 20%;
                position : relative;
                .icon-img{
                    position : absolute;
                    left:0;
                    right:0;
                    top:0;
                    bottom:.44rem;
                    box-sizing:border-box;
                    padding:.1rem;
                    .icon-imgcontent{
                        height:100%;
                        margin : 0 auto;
                        display : block;
                    }
                }
                .icon-desc{
                    position : absolute;
                    left:0;
                    right:0;
                    bottom:0;
                    line-height : .44rem;
                    height:.44rem;
                    color : #333;
                    text-align : center;
                }
            }
        }
        .headline{
            height:0;
            padding-bottom:15%;
            position : relative;
            display : flex;
            .title{
                position:absolute;
                left:.1rem;
                top : .2rem;
                display : block;
                width: .7rem;
                height: .7rem;
                background : url(//pics.lvjs.com.cn/mobile/node_pro/projects/homepage/static/images/toutiao.png?v=2018);
                background-size : .7rem .7rem;
            }
            .swiper{
                width:75%;
                height :0;
                padding-bottom:15%;
                margin:0 10% 0 15%;
                overflow : hidden;
                p{
                    line-height:1.2rem;
                    text-indent : .3rem;
                    font-size:12px;
                }
            }
            .more{
                position:absolute;
                right : .2rem;
                top : .5rem;
                display : block;
                width : .16rem;
                height:.16rem;
                border-top : 1px solid #999;
                border-right : 1px solid #999;
                transform : rotate(45deg);
            }
        }
    }
</style>
