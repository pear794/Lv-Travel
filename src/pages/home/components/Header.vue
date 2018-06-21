<template>
    <div class="header" :style="opacityStyle">
        <div class="header-city" :on="handleScroll">
            <span class="cityClick">{{ city }}</span>
        </div>
        <div class="header-search">
            <span class="iconfont icon-search">&#xe61a;</span><span class="search-holder">目的地/景点/酒店/邮轮</span>
        </div>
        <div class="header-luck">
            <span class="icon-luck"></span>
        </div>
        <div class="header-account">
            <span class="icon-account"></span>
        </div>
    </div>
</template>

<script>
    export default {
        name : 'HomeHeader',
        data (){
            return {
                city : '郑州',
                opacityStyle : {
                    opacity : 1,
                    background : 'rgba(255,255,255,0)'
                }
            }
        },
        methods : {
            handleScroll (){
                const top = document.documentElement.scrollTop;
                let opacity = top / 140;
                if(top > 60 && top < 300) {
                    this.opacityStyle = {
                        opacity,
                        background: '-webkit-gradient(linear, 0 0, 100% 0, from(rgb(254, 81, 111)), to(rgb(254, 104, 108))) rgb(255, 255, 255)'
                    }
                }else if(top == 0){
                    this.opacityStyle = {
                        background: 'rgba(255,255,255,0)'
                    }
                }
            }
        },
        /* 页面加载就进行的生命周期函数 */
        activated (){
            window.addEventListener('scroll',this.handleScroll);
        }
    }
</script>

/* scoped可以限制当前的样式只对当前的组件有效 */
<style lang="stylus" scoped>
    @import '~styles/varible.styl'
    .header{
        width : 100%;
        max-width : 640px;
        min-width : 320px;
        margin : 0 auto;
        height : .9rem;
        line-height : .9rem;
        display : flex;
        padding:7px 5px 6px 15px;
        box-sizing : border-box;
        position: fixed;
        z-index : 1100;
        .header-city{
            width : 1.1rem;
            height : .6rem;
            line-height : .6rem;
            float : left;
            letter-spacing : 2px;
            .cityClick{
                font-size: 14px;
                color: #fff;
                width: auto;
                position: relative;
            }
            .cityClick::after{
                content : '';
                width: 5px;
                height: 5px;
                border-top: 1px solid #fff;
                border-right: 1px solid #fff;
                transform: rotate(135deg);
                position: absolute;
                top: 4px;
                right: -12px;
            }
        }
        .header-search{
            flex : 1;
            height : .6rem;
            line-height : .6rem;
            border-radius : 45px;
            color: #999;
            background #fff;
            margin-left : 5px;
            padding-left: 13px;
            overflow : hidden;
            .icon-search{
                display : block;
                float : left;
                margin-right:5px;
                color: #999;
                width:18px;
                height:18px;
                font-weight:bold;
                font-size:18px;
            }
            .search-holder{
                display : block;
                float : left;
                font-size:14px;
            }
        }
        .header-luck{
            float : right;
            width : .8rem;
            position : relative;
            .icon-luck{
                width:.4rem;
                height:.4rem;
                position:absolute;
                left:0;
                right:0;
                top:0;
                bottom:0;
                margin:auto;
                display : block;
                background-repeat: no-repeat;
                background-position: center;
                background-size:.4rem;
                background-image: url(https://pics.lvjs.com.cn/pics/super/2018/06/1528970917_36092.png);
            }
        }
        .header-account{
            float : right;
            width : .7rem;
            position : relative;
            .icon-account{
                width:.4rem;
                height:.4rem;
                display : block;
                background-repeat: no-repeat;
                background-position: center;
                background-size:.4rem;
                position:absolute;
                left:0;
                right:0;
                top:0;
                bottom:0;
                margin:auto;
                background-image: url(//pics.lvjs.com.cn/mobile/node_pro/projects/homepage/static/images/my.png?v=2018);
            }
        }
    }
</style>
