<template>
    <div class="bigIcon">
        <div class="content">
            <ul class="tickets style_1">
                <li>
                    <div>
                        <a href="#" style="background-image: url(https://pics.lvjs.com.cn/pics/super/2018/06/1528363908_16584.png);"></a>
                    </div>
                </li>
                <li class="height_li">
                    <div><a href="#">境外门票</a></div>
                    <div><a href="#">国内机票</a></div>
                </li>
                <li class="height_li">
                    <div><a href="#">火车票 · 汽车票</a></div>
                    <div><a href="#">邮轮</a></div>
                </li>
            </ul>
            <ul class="hotel">
                <li>
                    <div>
                        <a href="#" style="background-image: url(https://pics.lvjs.com.cn/pics/super/2018/05/1526291433_30876.png);"></a>
                    </div>
                </li>
                <li><div><a href="#">酒 + 景</a></div></li>
                <li><div><a href="#">机 + 票</a></div></li>
            </ul>
            <ul class="travel style_1">
                <li>
                    <div>
                        <a href="#" style="background-image: url(https://pics.lvjs.com.cn/pics/super/2018/02/1517903091_27390.png);"></a>
                    </div>
                    <div><a href="#">康旅专区</a></div>
                </li>
                <li>
                    <div><a href="#">国内游</a></div>
                    <div><a href="#">定制游</a></div>
                </li>
                <li>
                    <div><a href="#">出境游</a></div>
                    <div><a href="#">跟团游</a></div>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name : 'HomeSubnav'
    }
</script>

<style lang="stylus" scoped>
    .content {
        position : relative;
        width : 100%;
        height:100%;
    }
    .bigIcon{
        width : 100%;
        height:4.2rem;
        overflow:hidden;
        padding : 0 5px 0 5px;
        box-sizing:border-box;
        background:#fff;
        ul{
            border-radius: 0.2rem .2rem 0 0;
            width:100%;
            position : absolute;
            left:0;
            li{
                float:left;
                height:100%;
                text-align:center;
                border-right: 1px solid rgba(255,255,255,.45);
                box-sizing:border-box;
                a{
                    color:#fff;
                    width:100%;
                    height:100%;  
                    display : block;
                    background-repeat: no-repeat;
                    background-size: 100% 100%;
                }
            }
            .height_li div:nth-of-type(1){
                height:0.84rem;
                a{
                    height:0.84rem;
                    line-height : 0.84rem;
                }
            }
            .height_li div:nth-of-type(2){
                height:1.04rem;
                a{
                    height:1.04rem;
                    line-height : 1.04rem;
                }
            }
        }
        .style_1 li{
            width:33.5%;
            div{
                width:100%;
                height:50%;
                border-bottom: 1px solid rgba(255,255,255,.45);
                box-sizing:border-box;
            }
        }
        .tickets {
            height:1.86rem;
            background: -webkit-gradient(linear,left top,right bottom,from(#FD3C71),to(#FF6D6D));
            z-index:10;
            li:nth-of-type(1){
                width:33%;
                div{
                    width:100%;
                    height:100%;
                }
            }
        }
        .hotel{
            height:1.02rem;
            background: -webkit-gradient(linear,left top,right bottom,from(#4189EA),to(#5DAEED));
            z-index:20;
            top:1.7rem;
            li:nth-of-type(1){
                width:33%;
                div{
                    width:100%;
                    height:100%;
                }
            }
            li{
                width:33.5%;
                line-height:0.94rem;
            }
        }
        .travel{
            height:1.68rem;
            bottom:0;
            z-index:30;
            background: -webkit-gradient(linear,left top,right bottom,from(#20B79C),to(#5ECE6C));
            border-radius: 10px;
            li:nth-of-type(1){
                width:33%;
                text-align:left;
                text-indent : 0.5rem;
                div{
                    width:100%;
                    height:50%;
                }
            }
            li{
                line-height:0.84rem;
            }
        }
    }
</style>
