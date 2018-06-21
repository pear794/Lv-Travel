<template>
    <div class="home">
        <home-header></home-header>
        <home-swiper></home-swiper>
        <home-subnav></home-subnav>
        <home-icons></home-icons>
        <home-goal></home-goal>
    </div>
</template>

<script>
    import HomeHeader from './components/Header'
    import HomeSwiper from './components/Swiper'
    import HomeSubnav from './components/Subnav'
    import HomeIcons from './components/Icons'
    import HomeGoal from './components/Goal'
    export default {
        name : 'Home',
        components : {
            HomeHeader,
            HomeSwiper,
            HomeSubnav,
            HomeIcons,
            HomeGoal
        }
    }
</script>

<style lang="stylus" scoped>
    .home{
        max-width : 640px;
        min-width : 320px;
        margin : 0 auto;
        height : 2000px;
        position : relative;
        background: #efeff7;
    }
</style>
