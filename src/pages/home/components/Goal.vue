<template>
    <div class="banner">
        <div class="title">
            <h3>- 热门目的地 -</h3>
            <p>为您推荐当季全球好去处</p>
            <div class="more"></div>
        </div>
        <div class="swiper">
            <swiper :options="swiperOption" class="slide-box">
                <swiper-slide class="content" v-for="item in contentList" :key="item.id">
                    <div class="top-content">
                        <div class="content-bg">
                            <img class="content-img" :src="item.contentImg" />
                        </div>
                        <div class="content-title">
                            <span class="big-title">{{ item.city }}</span>
                            <span class="small-title">{{ item.people }}人去过</span>
                        </div>
                        <div class="sub-content">
                            <div class="left-box main-content">
                                <div class="bg-box">
                                    <img class="box-img" :src="item.boxImg.left">
                                    <span class="box-icon">{{ item.title }}</span>
                                </div>
                                <span class="box-introduce">{{ item.introduce.left}}</span>
                                <p class="box-price"><span class="orange">¥<strong>{{ item.price.left }}</strong></span>起</p>
                            </div>
                            <div class="right-box main-content">
                                <div class="bg-box">
                                    <img class="box-img" :src="item.boxImg.right">
                                    <span class="box-icon">{{ item.title }}</span>
                                </div>
                                <span class="box-introduce">{{ item.introduce.right}}</span>
                                <p class="box-price"><span class="orange">¥<strong>{{ item.price.right }}</strong></span>起</p>
                            </div>
                        </div>
                    </div>
                    <div class="footer">更多{{ item.city }}好产品<span><i></i></span></div>
                </swiper-slide>
            </swiper>
        </div>
    </div>
</template>

<script>
    export default {
        name : 'HomeGoal',
        data (){
            return {
                swiperOption : {
                    slidesPerView: 'auto',
                    spaceBetween: 15
                },
                contentList : [
                    {
                        id : '001',
                        city : '三亚',
                        people : '10727',
                        contentImg : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/09/C_20130709-469277_360_270.jpg',
                        boxImg : {
                            left : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2016-12-02/0fe0ec9b-59e1-4073-80ea-6bee1f2a8d82_480_320.jpg',
                            right : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2018-03-15/da8f2622-9e41-4514-bc41-5ae8f90dd9d9_480_320.jpg',
                        },
                        title : '自由行 | 全国出发 ',
                        introduce : {
                            left : '【爆款返场特卖 俯瞰三亚鹿城夜景】三亚柏瑞精品海景酒店豪华市景房连住2晚＋每日精致双人早餐＋网红空中泳池＋私家沙滩＼第一市场＼鹿回头山顶公园＼夏日百货',
                            right : '三亚 5天4晚 【春暖花开·快来“跳”海·双湾精选】三亚康年酒店2晚＋亚龙湾凯莱仙人掌酒店2晚，康年双人BBQ，三亚湾一线海景，儿童中心，蜜月求婚，无边际泳池，70米高空透明泳池，亚龙湾高性价比',
                        },
                        price : {
                            left : '398',
                            right : '2998'
                        }    
                    },
                    {
                        id : '002',
                        city : '珠海',
                        people : '6393',
                        contentImg : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2017-03-15/685f0797-a237-49dd-953c-8c5fd3eba227_360_270.jpg',
                        boxImg : {
                            left : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2018-04-28/bb4fb904-dd19-46e2-89da-111c571fd899_480_320.jpg',
                            right : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2017-09-07/f6d4e1a8-2b6b-475c-bcfa-d1a52170fc81_480_320.jpg',
                        },
                        title : '自由行 | 全国出发 ',
                        introduce : {
                            left : '珠海长隆海洋王国',
                            right : '珠海长隆国际马戏城（原珠海长隆横琴岛剧院）',
                        },
                        price : {
                            left : '30',
                            right : '225'
                        }    
                    },
                    {
                        id : '003',
                        city : '广州',
                        people : '13333',
                        contentImg : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2017-03-15/22d09ab3-b138-49bb-b41d-2fa29c5b8cb6_360_270.jpg',
                        boxImg : {
                            left : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2016-07-22/c8b7f433-8fab-4be1-b8f1-9e93f6577671_480_320.jpg',
                            right : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2015-06-02/5282b011-3663-4111-88c6-ff3544e6bef3_480_320.jpg',
                        },
                        title : '自由行 | 全国出发 ',
                        introduce : {
                            left : '【特卖】广州长隆香江大酒店1晚，享幸福快乐时光',
                            right : '广州长隆白虎自助餐厅',
                        },
                        price : {
                            left : '199',
                            right : '176'
                        }    
                    },
                    {
                        id : '004',
                        city : '丽江',
                        people : '15055',
                        contentImg : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2015-06-10/3b8f4915-f8d1-4135-ad2f-e256d46612d6_360_270.jpg',
                        boxImg : {
                            left : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2018-01-16/0c0f0b3a-ae74-41ca-a24f-d3bb85fdbf71_480_320.jpg',
                            right : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2015-11-30/14dd981b-e1b0-4f4a-a6b5-4b12079b959a_480_320.jpg',
                        },
                        title : '自由行 | 全国出发 ',
                        introduce : {
                            left : '丽江 2天1晚 【丽江慢游特卖】住1晚在云端客栈(在水一方店)＋双人早餐＋前台水果、茶、鲜花饼免费品尝',
                            right : '玉龙雪山',
                        },
                        price : {
                            left : '299',
                            right : '65'
                        }    
                    },
                    {
                        id : '005',
                        city : '上海',
                        people : '26338',
                        contentImg : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2016-12-26/eabfdeae-eece-4773-af31-5e55a01cb5dc_360_270.jpg',
                        boxImg : {
                            left : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2018-06-18/7363736d-360b-4f68-8514-adda43f0b2b2_480_320.jpg',
                            right : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2018-05-31/26de07ec-4b86-46ab-bd8d-e7122ac9ec08_480_320.jpg',
                        },
                        title : '自由行 | 全国出发 ',
                        introduce : {
                            left : '上海迪士尼乐园',
                            right : '上海玛雅海滩水公园',
                        },
                        price : {
                            left : '299',
                            right : '80'
                        }    
                    },
                    {
                        id : '006',
                        city : '大理',
                        people : '7176',
                        contentImg : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2017-05-09/772f0452-7983-467c-958d-7ee025844d5e_360_270.jpg',
                        boxImg : {
                            left : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2018-05-10/12cc89a2-326b-4733-847d-987972459882_480_320.jpg',
                            right : 'https://pics.lvjs.com.cn/pics//uploads/pc/place2/2016-08-19/69da8c78-93ca-4058-9ecc-34dafea343c8_480_320.jpg',
                        },
                        title : '自由行 | 全国出发 ',
                        introduce : {
                            left : '大理 2天1晚 【大理漫游特卖】住1晚既见·南国精品客栈＋双人早餐＋欢迎水果＋延迟退房＋入住期间免费WIFI【步行即达古城却没有古城的喧嚣】',
                            right : '昆明、大理、丽江、泸沽湖双飞7日游([纯玩零购物]丽进昆出，不走回头路，BBQ自助烧烤，赠丽水金沙表演 洱海大游床，上玉龙雪山享半山温泉，泸沽湖环湖游，赠送篝火晚会)',
                        },
                        price : {
                            left : '460',
                            right : '3298'
                        }    
                    },
                ]
            }
        }
    }
</script>

<style lang="stylus" scoped>
    .banner{
        width : 100%;
        padding-top : .2rem;
        padding-left : .2rem;
        padding-bottom : .2rem;
        margin-top : .2rem;
        overflow : hidden;
        background : #fff;
        box-sizing:border-box;
        .title{
            height : 1rem;
            line-height : .5rem;
            width : 100%;
            text-align :center;
            position : relative;
            h3{
                font-size:16px;
                color : #333;
                font-weight:500;
            }
            p{
                font-size: 12px;
                color: #999;
                line-height: 12px;
                margin-top: 5px;
            }
            .more{
                width : .36rem;
                height : .36rem;
                border:1px solid #8E8E8E;
                border-radius : 50%;
                position : absolute;
                top : .2rem;
                right : .2rem;
            }
            .more::before{
                content : ' ';
                width : .12rem;
                height : .12rem;
                position : absolute;
                left : 0;
                right : 0;
                top : 0;
                bottom : 0;
                margin:auto;
                display : block;
                border-top: 1px solid #999;
                border-right: 1px solid #999;
                transform: rotate(45deg);
                -webkit-transform : rotate(45deg);
            }
        }
        .swiper >>> .swiper-container{
            overflow : visible !important;
            margin:0 !important;
        }
        .swiper{
            width:100%;
            height:6.28rem;
            .slide-box{
                width:90%;
                height:6.28rem;
                .content{
                    width : 100%;
                    height: 100%;
                    .top-content{
                        width:100%;
                        height:5.3rem;
                        position : relative;
                        .content-img{
                            width : 100%;
                            height : 3.04rem;
                            position : absolute;
                            left:0;
                            top:0;
                            border-radius : 4px;
                            z-index : 5;
                        }
                        .content-title{
                            position : absolute;
                            width:60%;
                            height:1rem;
                            z-index:6;
                            top:.3rem;
                            left:.3rem;
                            color:#fff;
                            .big-title{
                                font-size:20px;
                                line-height : 20px; 
                            }
                            .small-title{
                                font-size: 11px;
                                line-height: 20px;
                                margin-left: 30px;
                                position: relative;
                            }
                            .small-title::before{
                                position: absolute;
                                bottom: 3px;
                                left: -15px;
                                content: "";
                                width: 11px;
                                height: 11px;
                                background: url(//pics.lvjs.com.cn/mobile/node_pro/projects/homepage/static/images/playerNum.gif) center no-repeat;
                                background-size: 11px 11px;
                            }
                        }
                        .sub-content{
                            position : absolute;
                            width:96%;
                            height:4rem;
                            bottom:0;
                            left:2%;
                            z-index:7;
                            .left-box{
                                float : left;
                            }
                            .right-box{
                                float : right;
                            }
                            .main-content{
                                width:48%;
                                padding:3px;
                                height:4rem;
                                background #fff;
                                box-sizing:border-box;
                                box-shadow: 0 0 15px 0 rgba(0,0,0,.15);
                                .bg-box{
                                    position : relative;
                                    height:111px;
                                    .box-img{
                                        width:100%;
                                        hright:100%;
                                    }
                                    .box-icon{
                                        position : absolute;
                                        top: 0;
                                        left: 0;
                                        display : block;
                                        background: #363640;
                                        padding: 0 5px;
                                        height: 16px;
                                        line-height: 16px;
                                        font-size: 10px;
                                        color: #FFF;
                                        border-bottom-right-radius: 6px;
                                    }
                                }
                                .box-introduce{
                                    width:100%;
                                    height:.6rem;
                                    display :block;
                                    overflow:hidden;
                                    display: -webkit-box;
                                    -webkit-box-orient: vertical;
                                    -webkit-line-clamp: 2;
                                    font-size: 12px;
                                    color: #333;
                                    line-height : .3rem;
                                    margin: 5px 2px 0;
                                }
                                .box-price{
                                    margin: 5px 2px 0;
                                    font-size: 10px;
                                    color: #999;
                                    line-height: 10px;
                                    padding:3px 0 3px 5px;
                                    .orange{
                                        color: #F60;
                                        strong{
                                            font-size: 16px;
                                            line-height: 16px;
                                            font-weight: 600;
                                            padding:0 3px 0 2px;
                                        }
                                    }
                                }
                            }
                        }
                    }
                    .footer{
                        width:100%;
                        height:.98rem;
                        line-height : .98rem;
                        text-align : center;
                        font-size: 15px;
                        color: #5CA2F8;
                        span{
                            width: 13px;
                            height: 13px;
                            background: #5CA2F8;
                            border-radius: 100%;
                            display: inline-block;
                            margin-left:5px;
                            margin-top:3px;
                            i{
                                display: block;
                                width: 5px;
                                height: 5px;
                                margin-top: 3px;
                                margin-left: 3px;
                                transform: rotate(45deg);
                                -webkit-transform: rotate(45deg);
                                border-top: 1px solid #fff;
                                border-right: 1px solid #fff;
                            }
                        }
                    }
                }
            }
        }
    }
</style>
