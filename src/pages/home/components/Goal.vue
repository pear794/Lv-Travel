<template>
    <div class="banner">
        <div class="title">
            <h3>- 热门目的地 -</h3>
            <p>为您推荐当季全球好去处</p>
            <div class="more"></div>
        </div>
        <div class="swiper">
            <div class="slide-box">
                <div class="content">
                    <div class="content-bg">
                        <img class="content-img" src="https://pics.lvjs.com.cn/pics//uploads/pc/place2/09/C_20130709-469277_360_270.jpg" />
                    </div>
                    <div class="content-title">
                        
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name : 'HomeGoal'
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
        .swiper{
            width:100%;
            .slide-box{
                width:95%;
                .content{
                    width : 100%;
                    height: 5.12rem;
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
                }
            }
        }
    }
</style>
